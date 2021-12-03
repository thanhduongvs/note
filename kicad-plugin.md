# kicad-plugin

https://docs.kicad.org/doxygen-python/

```
import pcbnew
from pcbnew import *
board = GetBoard()
board.GetFootprints()
bds=board.GetDesignSettings()
stackup=bds.GetStackupDescriptor()
bds.GetCopperLayerCount()
bds.GetBoardThickness()

# R1, U1
board.GetFootprints()[0].GetReference()

# 10K, 0.1uF
board.GetFootprints()[0].GetValue()

# 2, 10
board.GetFootprints()[0].GetPadCount()

# 1, A1
board.GetFootprints()[0].Pads()[0].GetPadName()

# SMD
board.GetFootprints()[0].Pads()[0].GetTypeName()

# 'unconnected-(U1-PadA1)'
net=board.GetFootprints()[0].Pads()[0].GetNetname()
board.GetNetcodeFromNetname(net)	#15

PAD_ATTRIB_PTH
PAD_ATTRIB_SMD
PAD_ATTRIB_CONN
PAD_ATTRIB_NPTH
board.GetFootprints()[0].Pads()[0].GetAttribute()


board.FindFootprintByReference('U1').GetPadCount()
#{'Category': 'IC', 'Sheetfile': 'as.kicad_sch', 'Sheetname': '', 'name': '', 'pad': ''}
board.FindFootprintByReference('U1').GetProperties()
#'FOOTPRINT'
board.FindFootprintByReference('U1').GetClass()
board.FindFootprintByReference('U1').GetPropertiesNative()





Net Inspector
Show zero pad nets
Via Length

https://docs.kicad.org/doxygen-python/
DIALOG_NET_INSPECTOR::calculateViaLength
DIALOG_NET_INSPECTOR::onUnitsChanged
DIALOG_NET_INSPECTOR::onBoardChanged
```
