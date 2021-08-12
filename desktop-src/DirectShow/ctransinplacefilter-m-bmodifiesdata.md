---
description: La variabile \_ membro m bModifiesData indica se il filtro modifica i dati di esempio ricevuti. Il valore viene impostato nel costruttore CTransInPlaceFilter, ma il valore predefinito è TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: Membro CTransInPlaceFilter::m_bModifiesData (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654880"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Membro CTransInPlaceFilter::m \_ bModifiesData

La `m_bModifiesData` variabile membro indica se il filtro modifica i dati di esempio ricevuti. Il valore viene impostato nel costruttore **CTransInPlaceFilter,** ma il valore predefinito è **TRUE.**

## <a name="syntax"></a>Sintassi


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Osservazioni

Questa variabile influisce sul modo in cui il filtro negozia l'allocatore. Se il valore è **TRUE,** il filtro non può usare un allocatore di sola lettura per entrambe le connessioni pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




