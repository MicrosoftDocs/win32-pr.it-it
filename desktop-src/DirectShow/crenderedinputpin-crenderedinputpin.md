---
description: Metodo del costruttore.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Costruttore CRenderedInputPin. CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329373"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a>Costruttore CRenderedInputPin. CRenderedInputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pObjectName* 
</dt> <dd>

Stringa contenente il nome di debug dell'oggetto. Per ulteriori informazioni, vedere la [**classe CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato. Può trattarsi della stessa sezione critica del blocco filter, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> <dt>

*pName* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del PIN (usato anche come identificatore del pin).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amextra. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




