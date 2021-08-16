---
description: Se il bit controllo bitmap è impostato, il testo nel controllo viene sostituito da un'immagine bitmap. La colonna Text nella tabella Control è una chiave esterna nella tabella Binary.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Attributo del controllo Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cd7ea8186d1ed16de71ae9974bb67a082142ed3e921d023ad905d4f47bbc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638740"
---
# <a name="bitmap-control-attribute"></a>Attributo del controllo Bitmap

Se il bit controllo bitmap è impostato, il testo nel controllo viene sostituito da un'immagine bitmap. La colonna Text nella [tabella Control è](control-table.md) una chiave esterna nella tabella [Binary](binary-table.md).

Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna Text della [tabella Control](control-table.md).

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

 

[Pulsante](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit Bitmap nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

La colonna Text nella tabella Control viene usata come chiave esterna per la tabella [Binary](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.

Non impostare i bit [Icona](icon-control-attribute.md) e Bitmap.

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



