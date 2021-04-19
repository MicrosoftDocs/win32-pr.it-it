---
description: Se questo bit è impostato, la barra di scorrimento si trova sul lato sinistro del controllo.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Attributo di controllo LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99505e66f6f49b0a148b80a96d68bbef70d0f2b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307252"
---
# <a name="leftscroll-control-attribute"></a>Attributo di controllo LeftScroll

Se questo bit è impostato, la barra di scorrimento si trova sul lato sinistro del controllo.

Se questo bit non è impostato, la barra di scorrimento si trova sul lato destro del controllo.

## <a name="valid-controls"></a>Controlli validi

[ScrollableText](scrollabletext-control.md)

[VolumeCostList](volumecostlist-control.md)

[ComboBox](combobox-control.md)

[Elenco di directory](directorylist-control.md)

[DirectoryCombo](directorycombo-control.md)

[Modifica](edit-control.md)

[ListBox](listbox-control.md)

[ListView](listview-control.md)

[SelectionTree](selectiontree-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                             |
|---------|-------------|--------------------------------------|
| 128     | 0x00000080  | **msidbControlAttributesLeftScroll** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit LeftScroll nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



