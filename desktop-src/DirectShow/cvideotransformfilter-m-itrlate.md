---
description: Indica la fine dell'arrivo degli esempi nel renderer, in unità di tempo di riferimento. Sintassi.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
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
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330190"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Membro itrLate di CVideoTransformFilter:: m \_

Indica la fine dell'arrivo degli esempi nel renderer, in unità di tempo di riferimento. Sintassi

## <a name="syntax"></a>Sintassi


```C++
int m_itrLate;
```



## <a name="remarks"></a>Osservazioni

Quando il filtro riceve un messaggio di qualità da downstream, archivia il valore di latenza in questa variabile. Quando il filtro elimina i frame, questo valore viene aggiornato sottraendo la durata di ogni fotogramma.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




