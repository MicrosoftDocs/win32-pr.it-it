---
title: TEXT.scrollingAmount
description: L'attributo scrollingAmount specifica o recupera il numero di pixel che il testo sposta durante ogni movimento di scorrimento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT.scrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a8d5b703c02c2d3049f98a934980f1dbf8b1c5beceaca4d97158ea68c13db9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466961"
---
# <a name="textscrollingamount"></a>TEXT.scrollingAmount

**L'attributo scrollingAmount** specifica o recupera il numero di pixel che il testo sposta durante ogni movimento di scorrimento.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero positivo di lettura/scrittura **(** **int**) con valore predefinito 6.

## <a name="remarks"></a>Commenti

Per lo scorrimento uniforme, **scrollingAmount** deve essere di piccole dimensioni. Per il disegno veloce con grandi lacune, **scrollingAmount** deve essere maggiore. Se **scrolling** ="false", **scrollingAmount viene** ignorato.

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.scrolling**](text-scrolling.md)
</dt> </dl>

 

 





