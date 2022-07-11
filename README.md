// This source code is subject to the terms of the Mozilla Public License 2.0 at https://mozilla.org/MPL/2.0/
// © peacefulToucan67678

//@version=5
indicator("CCI BARS", overlay=true)
Source = input.source(hlc3)
Length = input.int(20)
cci = ta.cci(Source, Length)
color_0 = #00332a
color_1 = #056656
color_2 = #22ab94
color_3 = #42bda8
color_4 = #ace5dc
color_5 = #faa1a4
color_6 = #f77c80
color_7 = #f7525f
color_8 = #b22833
color_9 = #801922
barcolor(cci < -250  ? color_0  :  cci > -250  and cci <= -225 ? color_0 :  cci > -225 and cci <= -200 ? color_1 :cci > -200 and cci <= -175 ? color_1 :cci > -175 and cci <= -150 ? color_2 :cci > -150 and cci <= -125 ? color_2 :cci > -125 and cci <= -100 ? color_3 :cci > -100 and cci <= -75 ? color_3 :cci > -75 and cci <= -50 ? color_4 :cci > -50 and cci <= 0 ? color_4 :cci > 0 and cci <= 50 ? color_5 :cci > 50 and cci <= 75 ? color_5 :cci > 75 and cci <= 100 ? color_6 :cci > 100 and cci <= 125 ? color_6 :cci > 125 and cci <= 150 ? color_7 :cci > 150 and cci <= 175 ? color_7 :cci > 175 and cci <= 200 ? color_8 :cci > 200 and cci <= 225 ? color_8 :cci > 225 and cci <= 250 ? color_9 :cci > 250 ? color_9:na)
