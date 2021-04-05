---
description: Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi rimovibili. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Attributo di controllo RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751127"
---
# <a name="removablevolume-control-attribute"></a>Attributo di controllo RemovableVolume

Se questo bit è impostato, il controllo Mostra tutti i volumi interessati dall'installazione corrente più tutti i volumi rimovibili. Se questo bit non è impostato, il controllo Elenca i volumi nell'installazione corrente.

## <a name="valid-controls"></a>Controlli validi

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit RemovableVolume nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



