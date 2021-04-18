---
description: Se viene impostato il bit del controllo CDROMVolume, il controllo Mostra tutti i volumi nell'installazione corrente e tutti i volumi CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Attributo di controllo CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310996"
---
# <a name="cdromvolume-control-attribute"></a>Attributo di controllo CDROMVolume

Se viene impostato il bit del controllo CDROMVolume, il controllo Mostra tutti i volumi nell'installazione corrente e tutti i volumi CD-ROM.

Se questo bit non è impostato, il controllo Mostra tutti i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                              |
|---------|-------------|---------------------------------------|
| 524288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit CDROMVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



