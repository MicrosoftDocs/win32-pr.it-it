---
description: Se viene impostato il bit del controllo FloppyVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i volumi floppy.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Attributo di controllo FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528183"
---
# <a name="floppyvolume-control-attribute"></a>Attributo di controllo FloppyVolume

Se viene impostato il bit del controllo FloppyVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i volumi floppy.

Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                               |
|---------|-------------|----------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit FloppyVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



