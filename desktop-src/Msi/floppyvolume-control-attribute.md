---
description: Se il bit di controllo FloppyVolume è impostato, il controllo mostra tutti i volumi coinvolti nell'installazione corrente più tutti i volumi floppy.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Attributo del controllo FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947012"
---
# <a name="floppyvolume-control-attribute"></a>Attributo del controllo FloppyVolume

Se il bit di controllo FloppyVolume è impostato, il controllo mostra tutti i volumi coinvolti nell'installazione corrente più tutti i volumi floppy.

Se questo bit non è impostato, il controllo elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit FloppyVolume nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



