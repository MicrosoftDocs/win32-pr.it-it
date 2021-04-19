---
title: TESTO. scrollingAmount
description: L'attributo scrollingAmount specifica o Recupera il numero di pixel spostati dal testo durante ogni spostamento dello scorrimento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Media Player di Windows TEXT. scrollingAmount
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328587"
---
# <a name="textscrollingamount"></a>TESTO. scrollingAmount

L'attributo **scrollingAmount** specifica o Recupera il numero di pixel spostati dal testo durante ogni spostamento dello scorrimento.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura positivo (**int**) con un valore predefinito di 6.

## <a name="remarks"></a>Commenti

Per lo scorrimento uniforme, **scrollingAmount** deve essere di dimensioni ridotte. Per il disegno veloce con grandi Gap, il **scrollingAmount** deve essere più grande. Se lo **scorrimento** è "false", **scrollingAmount** viene ignorato.

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

 

 





