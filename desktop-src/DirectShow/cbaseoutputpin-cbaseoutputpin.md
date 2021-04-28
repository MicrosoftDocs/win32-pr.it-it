---
description: 'Costruttore CBaseOutputPin.CBaseOutputPin : metodo del costruttore.'
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Costruttore CBaseOutputPin.CBaseOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9901591be32d431ebe53a2098456446a0126d26b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099569"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>Costruttore CBaseOutputPin.CBaseOutputPin

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseOutputPin(
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

Stringa contenente il nome di debug dell'oggetto. Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro che ha creato questo segnaposto.

</dd> <dt>

*Plock* 
</dt> <dd>

Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato. Può trattarsi della stessa sezione critica del blocco del filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> <dt>

*Pname* 
</dt> <dd>

Stringa di caratteri wide contenente il nome del segnaposto (usato anche come identificatore pin).

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i parametri vengono passati direttamente al [**costruttore CBasePin.**](cbasepin.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




