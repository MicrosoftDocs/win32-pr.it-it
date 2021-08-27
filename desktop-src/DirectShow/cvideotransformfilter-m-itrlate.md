---
description: Indica il ritardo degli esempi nel renderer, in unità di tempo di riferimento. Sintassi.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: Membro CVideoTransformFilter::m_itrLate (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075951"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Membro CVideoTransformFilter::m \_ itrLate

Indica il ritardo degli esempi nel renderer, in unità di tempo di riferimento. Sintassi

## <a name="syntax"></a>Sintassi


```C++
int m_itrLate;
```



## <a name="remarks"></a>Osservazioni

Quando il filtro riceve un messaggio di qualità da downstream, archivia il valore di ritardo in questa variabile. Quando il filtro elimina i fotogrammi, questo valore viene aggiornato sottraendo la durata di ogni fotogramma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




