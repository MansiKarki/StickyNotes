<!-- App.svelte -->
<script>
    import StickyNote from './StickyNote.svelte';
   import Note from './Note.svelte';
    let notes = [
      // { id: 1, content: 'Note 1' },Automatically add two notes
      // { id: 2, content: 'Note 2' },
          
    ];
    let newNoteContent = '';
    function addNote() {
      if (newNoteContent.trim() !== '') {
        notes = [...notes, { id: Date.now(), content: newNoteContent }];
        newNoteContent = '';
      }
    }
  </script>
  
  <div>
    <div>
      <textarea bind:value={newNoteContent}></textarea>
      <button on:click={addNote}>Add Note</button>
    </div>
  
    {#each notes as note (note.id)}
          <Note>
              <div class="con" contenteditable>{note.content}</div>
          </Note>
    {/each}
  </div>
  
  <style>
      .con
      {
      background: yellow;
      padding: 20px;
      width: 200px;
      color:black;
      text-align: center;
  }</style>