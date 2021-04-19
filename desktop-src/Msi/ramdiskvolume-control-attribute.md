---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi del disco RAM. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Attributo di controllo RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311720"
---
# <a name="ramdiskvolume-control-attribute"></a>Attributo di controllo RAMDiskVolume

Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi del disco RAM. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit RAMDiskVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



