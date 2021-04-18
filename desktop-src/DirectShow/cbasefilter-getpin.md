---
description: Il metodo GetPin recupera un PIN. La classe CEnumPins chiama questo metodo per enumerare i pin sul filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Metodo CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328947"
---
# <a name="cbasefiltergetpin-method"></a>CBaseFilter. GetPin, metodo

Il metodo **GetPin** recupera un PIN. La classe [**CEnumPins**](cenumpins.md) chiama questo metodo per enumerare i pin sul filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Indice in base zero del PIN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'oggetto [**CBasePin**](cbasepin.md) che implementa il PIN.

## <a name="remarks"></a>Commenti

È necessario implementare questo metodo virtuale puro nella classe derivata. Restituisce un puntatore al pin *n* sul filtro, indicizzato da zero. È possibile scegliere un ordine di indicizzazione arbitrario, purché l'ordinamento sia corretto. Se il filtro aggiunge o Elimina pin o le modifiche di ordinamento per altri motivi in fase di esecuzione, chiamare il metodo [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




