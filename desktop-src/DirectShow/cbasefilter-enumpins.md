---
description: 'Il metodo EnumPins enumera i pin in questo filtro. Questo metodo implementa il metodo IBaseFilter:: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Metodo CBaseFilter. EnumPins (Amfilter. h)
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
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330415"
---
# <a name="cbasefilterenumpins-method"></a>CBaseFilter. EnumPins, metodo

Il `EnumPins` metodo enumera i pin in questo filtro. Questo metodo implementa il metodo [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .

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

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                   | Descrizione                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente<br/>       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea un'istanza della classe di base [**CEnumPins**](cenumpins.md) e restituisce un puntatore a tale oggetto, di tipo **IEnumPins**. La classe **CEnumPins** chiama il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro per enumerare i pin sul filtro.

Se questo metodo ha esito positivo, l'interfaccia **IEnumPins** ha un conteggio dei riferimenti in attesa. Il chiamante deve rilasciare l'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




