### Task 7 kyu

[Task link](https://www.codewars.com/kata/563b662a59afc2b5120000c6)

In a small town the population is p0 = 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new inhabitants per year come to live in the town. How many years does the town need to see its population greater or equal to p = 1200 inhabitants?

At the end of the first year there will be:
1000 + 1000 * 0.02 + 50 => 1070 inhabitants

At the end of the 2nd year there will be:
1070 + 1070 * 0.02 + 50 => 1141 inhabitants (** number of inhabitants is an integer **)

At the end of the 3rd year there will be:
1141 + 1141 * 0.02 + 50 => 1213

It will need 3 entire years.


### My solution

```Java

class Arge {

    public static int nbYear(int p0, double percent, int aug, int p)
    {
        percent*=0.01;
        int years=0;
        while(p0<p)
        {
            years++;
            p0+=p0*percent+aug;
        }
        return years;
    }
}

```

### Favourite solution from code-wars

```Java

class Arge {
    static int nbYear(int p0, double percent, int aug, int p) {
        return p0 < p ? nbYear((int) (p0 * (percent / 100 + 1) + aug), percent, aug, p) + 1 : 0;
    }
}

```

I have learnt new construction "?", i didn't really know that it means if, haha

# Have a nice day!