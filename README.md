If you are exporting your bookmarks from a common browser, and you find that the
`.html` file is not well-styled for reading, then you may add this to it.

```
<style>

    /*  

    This is a <style/> for a 
    <!DOCTYPE NETSCAPE-Bookmark-file-1> 
    ;

    The XML structure is eccentric.
    For example, Chrome ( 2023-08 ) outputs :

        meta
        
        title
        
        h1              ... the gen0-folder-entity's NAME;
        dl              ... the gen0-folder-entity's CONTAINER;

            p           ... vacuous;
            
            dt          ... a gen1-child-entity;
                a           if the entity is a link, the LINK;

            dt          ... a gen1-child-entity;
                h3          if the entity is a folder, the folder NAME;
                dl          if the entity is a folder, the folder's CONTAINER; 
                    
                    dt  ... a gen2-child-entity ( etc. );
                p
            
        p

    */

    * {
        font-family:
            "SF UI Display",
            "Roboto Condensed",
            "Helvetica",
            "Tahoma",
            Sans
            ;
    }

    p {
        display:none;
    }

    dl {
        padding: 0 0 0 2rem;
        
        /* Indent each folder's container. */
    }

    dt > a {
        display: list-item;
        list-style-position: inside;
        list-style-type: "🔗 ";
    }

    dt > h3 {
        display: list-item;
        list-style-position: inside;
        list-style-type: "📁 ";
    }

</style>
```
