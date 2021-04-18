---
description: Se il bit del controllo ComboBox è impostato su una casella combinata, il campo Edit viene sostituito da un campo di testo statico. In questo modo si impedisce a un utente di immettere un nuovo valore e l'utente deve scegliere solo uno dei valori predefiniti.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Attributo del controllo combogroup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315481"
---
# <a name="combolist-control-attribute"></a>Attributo del controllo combogroup

Se il bit del controllo ComboBox è impostato su una casella combinata, il campo Edit viene sostituito da un campo di testo statico. In questo modo si impedisce a un utente di immettere un nuovo valore e l'utente deve scegliere solo uno dei valori predefiniti.

Se questo bit non è impostato, la casella combinata dispone di un campo di modifica.

## <a name="valid-controls"></a>Controlli validi

[ComboBox](combobox-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Descrizione                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit dell'oggetto ComboBox nella colonna attributi del record del controllo nella tabella dei [controlli](control-table.md).

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



