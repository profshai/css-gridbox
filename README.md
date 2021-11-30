# CSS-Grids


# Turn data into grids:

display: grid;

# Divide columns into 3 equally. Can also use --> repeat(3, 1fr):

grid-template-columns: 1fr 1fr 1fr;

# Best option is to divide grids into 12 by 1 fraction unit:

grid-template-columns: repeat(12, 1fr);

# Similar for the rows:

grid-template-rows: repeat(2, 2fr);

# To put a gap between grids

grid-gap: 3px;


# Define the grids by rows and columns: same result as above:
grid-template: repeat(2, 50px) / repeat(3, 1fr)

# Span whole row (2 ways are same):
grid-column: 1 / span 2; (when only two columns are involved)
grid-column: 1/-1; (regardless of the number of columns)

# Tries to fit all columns no matter the size of the page; uses the min 100px but if it cant fit a row, it reverts to 1fr:
grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));

# To let the grid conform to the columns misbehavior:
grid-auto-rows: 100px;

# Fills all gaps between grid_images:
grid-auto-flow: dense;

# Justify-content along the row axis:
justify-content: end; => can also use start or center;
justify-content: space-between; => put spaces between contents
justify-content: space-evenly; => put spaces evenly between and around contents;
justify-content: space-around; => put spaces evenly between contents only;

justify-self: center; =>  center a particular content

# Align content along the column axis:
align-self: end; =>  can also use start or center;

# Grid border:
border: 1px solid black;

# Auto-fit vs auto-fill:
grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); => tries to fit everything
grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); =>  doesn't fit but add new spaces
