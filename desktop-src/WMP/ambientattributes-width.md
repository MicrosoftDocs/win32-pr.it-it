---
title: AmbientAttributes. Width
description: L'attributo Width specifica o recupera la larghezza del controllo.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Media Player Windows AmbientAttributes. Width
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325591"
---
# <a name="ambientattributeswidth"></a>AmbientAttributes. Width

L'attributo **Width** specifica o recupera la larghezza del controllo.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **Integer** a 16 bit in lettura/scrittura (da 0 a 32.767) che rappresenta la larghezza del controllo in pixel. Il valore predefinito è zero o la larghezza dell'immagine specificata nell'attributo **Image** del controllo.

## <a name="remarks"></a>Commenti

Se la larghezza specificata è più stretta rispetto alla larghezza dell'immagine fornita, l'immagine verrà ritagliata. Se la larghezza è maggiore della larghezza dell'immagine, l'area di clic andrà oltre il limite dell'immagine. Indipendentemente dal valore assegnato a questo attributo, l'immagine non può superare la **visualizzazione** padre o la relativa **visualizzazione**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





