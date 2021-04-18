---
description: Se questo bit è impostato, il testo viene sostituito da un'immagine dell'icona e la colonna di testo nella tabella del controllo è una chiave esterna nella tabella binaria.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Attributo del controllo Icon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308904"
---
# <a name="icon-control-attribute"></a>Attributo del controllo Icon

Se questo bit è impostato, il testo viene sostituito da un'immagine dell'icona e la colonna di testo nella [tabella del controllo](control-table.md) è una chiave esterna nella [tabella binaria](binary-table.md).

Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna di testo della [tabella dei controlli](control-table.md).

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

[Pulsante](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere i bit dell'icona nella colonna attributi del record del controllo nella tabella del [controllo](control-table.md).

La colonna di testo nella tabella dei controlli viene utilizzata come chiave esterna per la [tabella binaria](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.

Non impostare sia l'icona che i bit [bitmap](bitmap-control-attribute.md) .

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



