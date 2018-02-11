# lucky_sevens
Write a function lucky_sevens?(numbers), which takes in an array of integers and returns true if any three consecutive elements sum to 7.
<br />
<code>
function sevens( $params )
{
    $array_count = count($params); //Count items in array
    //Check if params has 3 or more values.
    if ( $array_count >= 3 ){
        for($i=0; $i<$array_count;$i++) {
            if (isset($params[$i+2])) {
                if ( (($params[$i] + $params[$i+1]) + $params[$i+2]) == 7 ){
                    //return $params[$i] .' '. $params[$i+1] .' '. $params[$i+2];
                    return TRUE;
                }
            }
        }
        //return 'Notice: No results found!';
        return FALSE;
    } else {
        return 'Error: 3 or more values are required!';
    }
}

$numbers = [-2,1, 8, 0, 3, 20, 3, 1, 5, 5];
//dd($numbers);
$items = sevens($numbers); 
</code>
