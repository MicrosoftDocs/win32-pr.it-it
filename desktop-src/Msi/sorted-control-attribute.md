---
description: Se questo bit è impostato, gli elementi elencati nel controllo vengono visualizzati in un ordine specificato. Se il bit non è impostato, gli elementi vengono visualizzati in ordine alfabetico.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Attributo di controllo ordinato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049368"
---
# <a name="sorted-control-attribute"></a>Attributo di controllo ordinato

Se questo bit è impostato, gli elementi elencati nel controllo vengono visualizzati in un ordine specificato. Se il bit non è impostato, gli elementi vengono visualizzati in ordine alfabetico.

## <a name="valid-controls"></a>Controlli validi

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[Controllo ListView](listview-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesSorted** |



 

## <a name="remarks"></a>Commenti

Per ordinare gli elementi in una [casella combinata](combobox-control.md), includere il bit ordinato nella colonna attributi della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella colonna Order della [tabella ComboBox](combobox-table.md).

Per ordinare gli elementi in una [casella di riepilogo](listbox-control.md), includere il bit ordinato nella colonna Attributes della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella colonna Order della [tabella ComboBox](combobox-table.md).

Per ordinare gli elementi in un controllo [ListView](listview-control.md), includere il bit ordinato nella colonna attributi della [tabella dei controlli](control-table.md) e specificare l'ordine degli elementi nella [tabella ComboBox](combobox-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



