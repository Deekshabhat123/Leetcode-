class Solution:
    def convert(self, s: str, numRows: int) -> str:
        # Handle edge cases
        if numRows == 1 or numRows >= len(s):
            return s
        
        # Create a list of empty strings to hold each row
        rows = [""] * numRows
        add = 0  # This tracks the current row we are adding characters to
        incr = 1 # This tracks whether we're moving down (1) or up (-1) between rows
        
        # Iterate over each character in the string
        for i in s:
            rows[add] += i  # Append the character to the current row
            
            # If we're at the top row, start moving downward
            if add == 0:
                incr = 1
            # If we're at the bottom row, start moving upward
            elif add == numRows - 1:
                incr = -1
            
            # Update the row index (move up or down)
            add += incr
        
        # Join all the rows to form the final result
        return "".join(rows)
