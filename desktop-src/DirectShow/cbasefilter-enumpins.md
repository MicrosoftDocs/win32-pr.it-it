---
description: Il metodo EnumPins enumera i pin per questo filtro. Questo metodo implementa il metodo IBaseFilter::EnumPins.
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Metodo CBaseFilter.EnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cd0be44f768898a530eef20d3e4d5d082d230ff809133c0eb62ceb2308b524b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640581"
---
# <a name="cbasefilterenumpins-method"></a>Metodo CBaseFilter.EnumPins

Il `EnumPins` metodo enumera i pin su questo filtro. Questo metodo implementa il [**metodo IBaseFilter::EnumPins.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente<br/>       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea un'istanza della classe di base [**CEnumPins**](cenumpins.md) e restituisce un puntatore a tale oggetto di tipo **IEnumPins**. La **classe CEnumPins** chiama il metodo [**CBaseFilter::GetPin**](cbasefilter-getpin.md) del filtro per enumerare i pin nel filtro.

Se questo metodo ha esito positivo, **l'interfaccia IEnumPins** ha un conteggio dei riferimenti in sospeso. Il chiamante deve rilasciare l'interfaccia .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




