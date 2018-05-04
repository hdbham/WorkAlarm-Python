import time
import ctypes

# should take 1 break then 1 lunch followed by 2 more breaks in afternoon.
# trying to space breaks and lunches to enhance productivity

## settings set for 10 hour shift with 37 minutes of break and 30 min lunch

# settings for interval count
total_intervals = 4
lunch_time = 1
interval_count = 0

# settings for interval length
lunch_length = 30*60 # 11 mins
break_length = 11*60 # 11 mins
wait_time = 2*60*60+1*60 # 2.25 hours in between breaks


print("You logged in at " + time.ctime())
    
while inverval_count != total_intervals:
        time.sleep(wait_time + break_length)
        ctypes.windll.user32.MessageBoxA(0, "YOU CAN TAKE A BREAK!", "GOOD NEWS!", 0x40)
        print("Last break taken on "+ time.ctime())
        interval_count = interval_count +1
        
        
        if  break_count == lunch_time:
            time.sleep(wait_time + lunch_length)
            ctypes.windll.user32.MessageBoxA(0, "ITS TIME FOR LUNCH!! ", "GOOD NEWS!", 0x40 )
            print("lunch taken on "+ time.ctime())
            interval_count = interval_count +1
            
            
ctypes.windll.user32.MessageBoxA(0, "ITS TIME TO GO HOME!!!", "GOOD NEWS!", 0x40)
raise SystemExit(0)
