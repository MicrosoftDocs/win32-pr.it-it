---
description: Se viene impostato il bit del controllo FixedVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i dischi rigidi interni fissi.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Attributo di controllo FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880194"
---
# <a name="fixedvolume-control-attribute"></a>Attributo di controllo FixedVolume

Se viene impostato il bit del controllo FixedVolume, il controllo Mostra tutti i volumi necessari nell'installazione corrente più tutti i dischi rigidi interni fissi.

Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | Valore esadecimale | Costante                              |
|---------|-------------|---------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit FixedVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



