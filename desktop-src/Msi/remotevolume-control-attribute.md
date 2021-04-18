---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi remoti. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Attributo di controllo RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306574"
---
# <a name="remotevolume-control-attribute"></a>Attributo di controllo RemoteVolume

Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi remoti. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                               |
|---------|-------------|----------------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesRemoteVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit RemoteVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



