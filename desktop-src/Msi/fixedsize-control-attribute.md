---
description: Se il bit FixedSize Control è impostato, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o le dimensioni.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attributo del controllo FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649701"
---
# <a name="fixedsize-control-attribute"></a>Attributo del controllo FixedSize

Se il bit FixedSize Control è impostato, l'immagine viene ritagliata o centrata nel controllo senza modificarne la forma o le dimensioni.

Se questo bit non è impostato, l'immagine viene estesa per adattarsi al controllo.

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

Per impostare questo attributo in un controllo, includere il bit FixedSize nella colonna Attributi del record del controllo nella [tabella Control](control-table.md).

L'impostazione del bit FixedSize non ha alcun effetto su un [](bitmap-control-attribute.md) [controllo CheckBox,](checkbox-control.md) [PushButton](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) se non è stata impostata né la bitmap né l'icona. [](icon-control-attribute.md)

L'impostazione del bit FixedSize non ha alcun effetto su un controllo Icon o su un controllo PushButton associato a un'icona, se i bit [IconSize](iconsize-control-attribute.md) non sono impostati.

Vedere [Attributi di controllo](control-attributes.md) e il controllo che è necessario creare in [Controlli](controls.md).

 

 



