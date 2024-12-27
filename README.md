# Code-Create-a-Spinning-Progress-Animation
Code: Create a Spinning Progress Animation


```python

import itertools
import sys
import time

def spinning_animation(duration=5, delay=0.1):
    """
    Create a spinning progress animation in the terminal.

    Args:
        duration (int): The duration of the animation in seconds.
        delay (float): The delay between each frame in seconds.
    """
    spinner = itertools.cycle(['|', '/', '-', '\\'])  # Frames of the spinner
    end_time = time.time() + duration  # Calculate end time

    print("Spinning Animation: Press Ctrl+C to stop.")
    while time.time() < end_time:
        sys.stdout.write(f"\r{next(spinner)}")  # Write the current frame
        sys.stdout.flush()  # Flush the output buffer
        time.sleep(delay)  # Pause for the delay
    print("\nAnimation Complete!")  # Message after completion

if __name__ == "__main__":
    spinning_animation()
```
