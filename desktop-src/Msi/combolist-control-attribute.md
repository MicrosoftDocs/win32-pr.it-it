---
description: Se il bit del controllo ComboList è impostato in una casella combinata, il campo di modifica viene sostituito da un campo di testo statico. Ciò impedisce a un utente di immettere un nuovo valore e richiede all'utente di scegliere solo uno dei valori predefiniti.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Attributo del controllo ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e0a53357d91c5c5a016f65e8e1e0fb341b15cae1ea2c6cf480e536fa109067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145380"
---
# <a name="combolist-control-attribute"></a>Attributo del controllo ComboList

Se il bit del controllo ComboList è impostato in una casella combinata, il campo di modifica viene sostituito da un campo di testo statico. Ciò impedisce a un utente di immettere un nuovo valore e richiede all'utente di scegliere solo uno dei valori predefiniti.

Se questo bit non è impostato, la casella combinata include un campo di modifica.

## <a name="valid-controls"></a>Controlli validi

[ComboBox](combobox-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Descrizione                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere il bit ComboList nella colonna Attributes del record del controllo nella [tabella Control](control-table.md).

Vedere [Attributi di](control-attributes.md) controllo e il controllo che è necessario creare in [Controlli](controls.md).

 

 



