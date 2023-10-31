<!-- StickyNote.svelte -->
<script>
    export let content = '';
  </script>
  
  <div class="sticky-note">
    {content}
  </div>
  
  <style>
    .sticky-note {
      border: 2px solid #000;
      padding: 20px;
      margin: 10px;
          color:black;
    }
      
  </style>