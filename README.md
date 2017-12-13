# Javascript Jquery Plugin Range
Features:
1. Numeric, negative numeric, decimal ranges.
2. Rangers with step and snap.
3. Double handlers, multiple and single.
4. Can have max value.
5. Always returned array.
6. More theme: teal, green, red...
7. Make your own format returned values.
8. Can be vertical and horizontal.
# Usage
### 1. Include Jquery
### 2. Include Range
### 3. Add hidden input
```
<input class="new-range" type="hidden">
```
### 4. Call created hidden input
```
<script>
var new_range = $('.new-range').range(
{
  from: 0, 			 						// Handler from. Must have a number value, supporting a negative number;
  to: 100, 	 		 						// handler to. Must have a number value, supporting a negative number;
  max: 0, 			 						// Maximum from-to values. Must have a positive number value;
  step: 1, 			 						// Rounding handlers values to step;
  snap: false,	 						// Values from-to rounding previous setting. Add snap for rounding handlers position to step;
  format: 'N', 	 						// Format values handlers. Add N for value handlers. Other values will remain unchanged;
  forever: true, 						// Handlers shows forever, else only hover;
  single: false, 						// Only handler to;
  onselect: function() {}   // Callback function on select handler to step;
}
);
</script>
```
### 4.1 Call function update for desired settings
```
new_range.range('update', 20 /*to*/, 0 /*from*/); // update values handlers
```
### 5. Return values to and from
```
var result = new_range.range('value'); // returned an array
console.log(result);
```
