# Granville-Phillips-375_RS232
Granville Phillips 375 Convectron Controller RS232 Data Acquisition

This program allows you to read the data from a Granville Phillips 375 readout via RS232.

The delay is in there because if you read faster than the display updates, you get artificial zeros.

Known bug: Every now and then there will be a gap in data much larger than the defined readout period. I made it so that the
              LabVIEW graph updates continuously but the data is only saved at a set period. I think this causes issues sometimes
              giving the above problem. It is not a problem for me since I am doing time evolution readings on large scales, not
              short scale readings. Example is reading out every 1s but one of the gaps during flushing was 29s. The rest of the gaps
              were within 100ms of my desired period (which is fine for me). I just wanted to have the graph readout quckly in case of
              a random pressure spike without outputting huge data files for a 10hr run.
                
