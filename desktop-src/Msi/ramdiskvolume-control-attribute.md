---
description: Se questo bit è impostato, il controllo mostra tutti i volumi coinvolti nell'installazione corrente più tutti i volumi del disco RAM. Se questo bit non è impostato, il controllo elenca i volumi nell'installazione corrente.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Attributo del controllo RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9167c045a8437fff12c312999d71bd8fc2c7927f1ac8d3acf2260127b73cbb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129021"
---
# <a name="ramdiskvolume-control-attribute"></a>Attributo del controllo RAMDiskVolume

Se questo bit è impostato, il controllo mostra tutti i volumi coinvolti nell'installazione corrente più tutti i volumi del disco RAM. Se questo bit non è impostato, il controllo elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo , includere il bit RAMDiskVolume nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi e controlli](control-attributes.md) del [controllo](controls.md).

 

 



