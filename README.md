# OpenMC-Depletion-Volume-Update
Modification to OpenMC to update the cell volume during the depletion calculation for multi-physics coupling

Modifications:
abc.py: 
1. Line 714: check_greater_than('timestep', timestep, 0.0, True)
   Allowed for 0 time-step for iteration within a burnup step

results.py: 
1. Lines 509-251: def update_volumes(self, geometry)
   Define a function to update the cell volume in the depletion for multi-physics coupling

operator.py:
1. Line 170: volume_update=False
   Add a parameter to control update of the volume
2. Lines 215-218: 
   Update the volume or not
