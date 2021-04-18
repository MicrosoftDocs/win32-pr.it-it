---
description: Si tratta di una combinazione degli attributi RTLRO, RightAligned e LeftScroll dell'ordine di lettura da destra a sinistra.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Attributo di controllo BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311020"
---
# <a name="bidi-control-attribute"></a>Attributo di controllo BiDi

Si tratta di una combinazione degli attributi [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) dell'ordine di lettura da destra a sinistra.

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



| Decimal | Valore esadecimale | Costante                       |
|---------|-------------|--------------------------------|
| 224     | 0x000000E0  | **msidbControlAttributesBiDi** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit BiDi nella colonna attributi del record del controllo nella [tabella del controllo](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



