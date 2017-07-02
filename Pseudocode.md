<!DOCTYPE Pseudocode>

BEGIN AQUIREINFORMATION
  Get distance1
  Get distance 2
  Get SPEED_LIMIT
  import textfile #this should be done first before your previous 3 lines right?
  Get number of lines in textfile -1
  Counter = number or lines in textfile -1
END

BEGIN NUMBERPLATES
#Seeing that the textfile was imported in the previous subroutine, how is it accessed again here?
#Remember the scope of variables.
#What are you trying to achieve here?
  FOR every line in textfile
    split line #you can't do this in pseudocode.
    append textfile[2] to numberplates[]
END

BEGIN TIMES
  for every numberplate
    get times passed through each checkpoint #you are going to have to write pseudocode to get this - keep a counter
    IF number plate passes through checkpoint1 and checkpoint2
      timetaken = checkpoint2time - checkpoint1time
      averagespeed = distance1 / timetaken
        IF averagespeed > speedlimit
          add "numberplate checkpoint2 averagespeed" to speeding[]
        ENDIF
    ENDIF
    IF numberplate passes through checkpoint2 and checkpoint3
      timetaken = checkpoint3time - checkpoint2time
      averagespeed = distance2 / timetaken
        IF averagespeed > speedlimit
        add "numberplate checkpoint3 averagespeed" to speeding[]
        ENDIF
    ENDIF
END

BEGIN OUTPUT
  Print speeding[]
END
