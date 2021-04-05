---
description: Se viene impostato il bit del controllo FixedSize, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o la dimensione.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attributo di controllo FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751143"
---
# <a name="fixedsize-control-attribute"></a>Attributo di controllo FixedSize

Se viene impostato il bit del controllo FixedSize, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o la dimensione.

Se questo bit non è impostato, l'immagine viene allungata per adattarsi al controllo.

## <a name="valid-controls"></a>Controlli validi

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Icona](icon-control.md)

[Pulsante](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Commenti

Per impostare questo attributo su un controllo, includere il bit FixedSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).

L'impostazione del bit FixedSize non ha alcun effetto su una [casella](checkbox-control.md)di controllo, un [pulsante](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) se non è stata impostata né la [bitmap](bitmap-control-attribute.md) né l' [icona](icon-control-attribute.md) .

L'impostazione del bit FixedSize non ha alcun effetto su un controllo Icon o su un pulsante associato a un'icona se i bit [iconSize](iconsize-control-attribute.md) non sono impostati.

Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).

 

 



