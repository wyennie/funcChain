Requires OpenAI API key in your `.env` file.
```
OPENAI_API_KEY=<Your key here>
```

This takes two command line arguments (`language`, `task`) and outputs a function and a test of said function.



**Example**

input:

```bash
python main.py --language python --task 'Takes a number and returns the value of that number squared'
```

output:

```
>>>>>> GENERATED CODE


def square(num):
    return num ** 2

>>>>>> GENERATED TEST



def test_square():
    # Test case 1: Positive integer
    assert square(5) == 25
    
    # Test case 2: Negative integer
    assert square(-4) == 16
    
    # Test case 3: Zero
    assert square(0) == 0
    
    # Test case 4: Decimal number
    assert square(2.5) == 6.25
    
    # Test case 5: Large number
    assert square(100) == 10000
    
    # Test case 6: String input
    assert square("2") == 4 # Should raise TypeError
    
    # Test case 7: Boolean input
    assert square(True) == 1
    
    # Test case 8: List input
    assert square([2]) == 4 # Should raise TypeError
```

