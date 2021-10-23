# Hobbies

***Golf***
  
  I recently started playing golf and have been devloping my game. My favorite course to play locally is [Tanglewood in Fulton Missouri](https://www.tanglewoodfulton.com/).

***Motocross***
  
  I grew up racing motocross and it has always been a passion of mine. I started riding dirtbikes when I was 4 years old. Unfortuanitly after my father had an accident I stopped riding. However, I still follow the sport. I grew up racing against [Chase Sexton](https://rxi.iscdn.net/2018/12/175595_175086_fchondadec18action-cudby-130.jpg).

***Python***

  Recently I have been trying to become proficient in python. It is commonly used in the Finance industry. I think having this skill will give me an edge over my competitors.
  
  Below is an example of one of my code blocks:
  
```python
import math

hourly_labor_cost = 62.25  # dollars per hour
unit_of_wall_area = 350    # square feet requiring 1 gallon of paint
hours_labor_per_unit = 6   # hours of labor per unit of wall area

print ('Paint job cost estimator')

do_estimate = True
while(do_estimate):


    while(True):
        try:
            wall_area = float(input('Enter square feet of wall to paint: '))
            if (wall_area <= 0):
                print('Wall area must be a positive not negative.')
                continue
        except:
            print('Only numerical values are valid.')
            continue
        else:
            break

    while(True):
        try:
            paint_price = float(input('Enter the price of paint per gallon: '))
            if (paint_price <= 0):
                print('price must be a positive number not negative.')
                continue
        except:
            print('Only numerical values are valid.')
            continue
        else:
            break

    # requirements are to round up to whole gallons.

    gallons_of_paint = math.ceil(wall_area / unit_of_wall_area)
    
    paint_cost = gallons_of_paint * paint_price
    hours_of_labor = (wall_area / unit_of_wall_area) * hours_labor_per_unit
    labor_cost = hours_of_labor * hourly_labor_cost
    total_cost = paint_cost + labor_cost

    print ('Gallons of paint:', gallons_of_paint)
    print ('Hours of labor:', format(hours_of_labor, '.1f'))
    print ('Paint cost: $', format(paint_cost,'.2f'), sep='')
    print ('Labor cost: $', format(labor_cost,'.2f'), sep='')
    print ('Total cost: $', format(total_cost,'.2f'), sep='')

    another_estimate = input('\nWould you like to do another estimate? (y/n) ')
    if (another_estimate != 'y'):
        do_estimate = False
```

[Home Page](README.md) [Next Page](Page2.md)
