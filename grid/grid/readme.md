# Summary

### template
This will define the template of the container
### -gap
This will define the gaps between the cells
### -content
This will structure how the cells interact with each other
### -items
This will structure how the content inside the cells is structured


##   Manually fitting 3 200px columns
  grid-template-columns: 200px 200px 200px
  Using repeat function
  grid-template-columns: repeat(3,200px);

  fr probably means fraction
  grid-template-columns: 1fr 2fr 1fr 1fr; 


  grid-template-rows: repeat(10,50px); 


  Automatically fit in minimum 340px and maximum 1 fr. If theres more than 340px slack, it will fit 1 more grid item. It will wrap
  auto-fill behavior: “fill that row up! Add as many columns as you can. I don’t care if they’re mpty — they should all still show up

  auto-fit behvaior  : “make whatever columns you have fit into the available space. 
  Expand them as much as you need to fit the row size. Empty columns must not occupy any space. P
  ut that space to better use by expanding the filled (as in: filled with content/grid items) columns to fit the available row space.”

  tldr auto-fill blank space, auto-fit expands width to fit 100% width
  
## Good way of displaying fixed size element. If you want dynamic then use flexbox instead
  grid-template-columns: repeat(auto-fit, minMaX(340px, 1fr)); 
  
    ## We can just define both rows and columns using grid-templates

  Since we have 4 rows but we only defined 3 rows, the fourth row will use default value
    grid-template: row / column  
    grid-template: repeat(4, 1fr)/ repeat(3, 1fr); 

  ## Gaps 
  column-gap: 40px;
  row-gap: 20px;
  ### shortcut
  gap: 40px 20px; 
  

  ------------------ 
  ##  MANAGING CELLS
  we use -items to align content inside cell
  we can use justify-items and align-items or we can use place-items
  justify-items: stretch is the default value
    center, end
  
  this is for X-axis 
  justify-items: center;   
  this is for Y-axis start, center, end 
  align-items: start;  

  place-items: end start; 

  ## Alignment in container 
  We use -content to align all cells in the container
  place-content: y-axis, x-axis
  justify is x-axis
  align is y-axis
  
   grid-template: repeat(4,200px)/ repeat(3, 200px); 
  start,center,end, space-between, space-around. space-evenly
   justify-content: center; 
  align-content: end;
  place-content: end center; 

### Auto-flow change row to column similar to flex-direction: column
  grid-auto-flow:column;
  grid-auto-columns: 100px;
  grid-auto-rows: 200px;
  grid-template: repeat(3,200px) / repeat(3,200px) ;




##  Grid item properties

### Short cut way of writing
  grid-column: 1 / span 2;
  grid-row: 1 / span 2;

### Long way  
  grid-column-start:1;
  grid-column-end: span 2;
  grid-row-start:1;
  grid-row-end: span 3;
  
##  Grid align x-axis and y-axis of self
  justify-self:end;
  align-self: start;
## shortcut 
  place-self: start end
  place-self: end center;
