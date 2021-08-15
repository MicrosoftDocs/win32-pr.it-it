---
description: Se questo bit è impostato, il testo viene sostituito da un'immagine icona e la colonna Text nella tabella Control è una chiave esterna nella tabella Binary.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Attributo del controllo Icon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2caeb407b86b888a5dd3b1c08f16d0893233f82cec29b92519c267b286ea121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315121"
---
# <a name="icon-control-attribute"></a>Attributo del controllo Icon

Se questo bit è impostato, il testo viene sostituito da un'immagine icona e la colonna Text nella tabella [Control](control-table.md) è una chiave esterna nella [tabella Binary](binary-table.md).

Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna Text della [tabella Control](control-table.md).

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

[Pulsante](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo in un controllo, includere i bit icona nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

La colonna Text nella tabella Control viene usata come chiave esterna per la tabella [Binary](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.

Non impostare i bit Icona [e Bitmap.](bitmap-control-attribute.md)

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



