---
title: TESTO. scrollingDelay
description: L'attributo scrollingDelay specifica o recupera l'intervallo di tempo tra i movimenti di scorrimento.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Media Player di Windows TEXT. scrollingDelay
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328585"
---
# <a name="textscrollingdelay"></a>TESTO. scrollingDelay

L'attributo **scrollingDelay** specifica o recupera l'intervallo di tempo tra i movimenti di scorrimento.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**int**) che specifica il ritardo in millisecondi. Il valore minimo è 30 e il valore predefinito è 85. Se viene specificato un valore minore del valore minimo, viene usato il valore predefinito.

## <a name="remarks"></a>Commenti

Se lo **scorrimento** è impostato su false, **scrollingDelay** viene ignorato.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. scorrimento**](text-scrolling.md)
</dt> </dl>

 

 





