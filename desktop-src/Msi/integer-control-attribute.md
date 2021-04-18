---
description: Se questo bit è impostato su un controllo, la proprietà associata specificata nella colonna proprietà della tabella dei controlli è un numero intero. Se questo bit non è impostato, la proprietà è un valore stringa.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Attributo controllo Integer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305964"
---
# <a name="integer-control-attribute"></a>Attributo controllo Integer

Se questo bit è impostato su un controllo, la proprietà associata specificata nella colonna proprietà della tabella dei [controlli](control-table.md) è un numero intero. Se questo bit non è impostato, la proprietà è un valore stringa.

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

[ComboBox](combobox-control.md)

[Modifica](edit-control.md)

[ListBox](listbox-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                          |
|---------|-------------|-----------------------------------|
| 16      | 0x00000010  | **msidbControlAttributesInteger** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit integer nella colonna attributi del record del controllo nella [tabella del controllo](control-table.md).

Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.

 

 



