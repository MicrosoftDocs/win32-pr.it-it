---
description: Se il bit cdROMVolume Control è impostato, il controllo mostra tutti i volumi nell'installazione corrente più tutti i volumi CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Attributo del controllo CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078041"
---
# <a name="cdromvolume-control-attribute"></a>Attributo del controllo CDROMVolume

Se il bit cdROMVolume Control è impostato, il controllo mostra tutti i volumi nell'installazione corrente più tutti i volumi CD-ROM.

Se questo bit non è impostato, il controllo visualizza tutti i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere il bit CDROMVolume nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



