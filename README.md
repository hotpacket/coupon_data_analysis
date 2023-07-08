# Coupon Data Analysis

In this project, we analyze a smartphone coupon [dataset](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation), collected via a survey on Amazon Mechanical Turk. The survey asked participants about several different driving scenarios (weather, passengers in car, etc.) and if they would accept food or drink coupons in those scenarios.

Our analysis can be found [here](https://github.com/hotpacket/coupon_data_analysis/prompt.ipynb). We focus our analysis on scenarios involving bar coupons, the age of the drivers, and whether the drivers have children.

### Finding 1: Frequent bargoers are likely to accept bar coupons. 

While the overall acceptance rate for bar coupons was 41%, drivers that visit bars four or more times per month were 76.9% likely to accept bar coupons. People over 25 who went to a bar at least once per month were 69.5% likely. People who went to a bar at least once per month, had a partner or friend(s) as passengers in the car, and worked in occupations other than farming, fishing, and forestry were 71.8% likely to accept.

### Finding 2: Younger people were more likely to accept all types of coupons 

The following table shows the overall coupon acceptance rate by age.

under 21    0.634369
      21    0.598191
      26    0.595936
      31    0.546346
      36    0.535254
      41    0.572736
      46    0.575802
 over 50    0.508949

We noted a particular dip in the 31 and 36 age ranges, and decided to investigate whether have kids influenced the acceptance decision.

### Finding 3: Having kids as passengers in the car negatively influenced coupon acceptance

The following table shows acceptance rates by passenger type.

No passengers 0.525804
Friend(s)     0.673438
Kid(s)        0.50497
Partner       0.595349

### Finding 4: Drivers in their thirties most likely to have children as passengers

As seen in the KDE plot below, drivers in their thirties were most likely to have children as passengers.

!([Child passenger KDE plot](https://github.com/hotpacket/coupon_data_analysis/blob/main/images/childpassengers.png)

### Finding 5: Of all drivers with child passengers, drivers in their thirties were least likely to accept coupons

The following table shows the acceptance rates for drivers with child passengers.

under 21    0.658824
      26    0.603306
      31    0.433628
      36    0.482143
      41    0.476471
      46    0.56962
 over 50    0.471338

Drivers in their thirties are most likely to have small children, which may make them least likely to change plans and accept unexpected coupons.

