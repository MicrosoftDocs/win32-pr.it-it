---
description: Se viene impostato il bit del controllo bitmap, il testo nel controllo viene sostituito da un'immagine bitmap. La colonna di testo nella tabella dei controlli è una chiave esterna nella tabella binaria.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Attributo di controllo bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881081"
---
# <a name="bitmap-control-attribute"></a>Attributo di controllo bitmap

Se viene impostato il bit del controllo bitmap, il testo nel controllo viene sostituito da un'immagine bitmap. La colonna di testo nella [tabella dei controlli](control-table.md) è una chiave esterna nella [tabella binaria](binary-table.md).

Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna di testo della tabella dei [controlli](control-table.md).

## <a name="valid-controls"></a>Controlli validi

[CheckBox](checkbox-control.md)

 

[Pulsante](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit bitmap nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).

La colonna di testo nella tabella dei controlli viene utilizzata come chiave esterna per la [tabella binaria](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.

Non impostare sia l' [icona](icon-control-attribute.md) che i bit bitmap.

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



