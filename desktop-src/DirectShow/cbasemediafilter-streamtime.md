---
description: "Metodo CBaseMediaFilter.StreamTime: il metodo StreamTime recupera l'ora corrente del flusso."
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Metodo CBaseMediaFilter.StreamTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096249"
---
# <a name="cbasemediafilterstreamtime-method"></a>Metodo CBaseMediaFilter.StreamTime

Il `StreamTime` metodo recupera l'ora corrente del flusso.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtStream* \[ Ref\]
</dt> <dd>

Riferimento a un [**oggetto CRefTime**](creftime.md) che riceve l'ora corrente del flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                      | Descrizione                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>             | Operazione completata.<br/>                         |
| <dl> <dt>**VFW \_ E \_ NO \_ CLOCK**</dt> </dl> | Non è disponibile alcun orologio di riferimento.<br/> |



 

## <a name="remarks"></a>Commenti

L'ora di flusso è definita come ora di riferimento corrente (come specificato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseMediaFilter::m \_ tStart**](cbasemediafilter-m-tstart.md)). Il timestamp di un campione multimediale specifica l'ora del flusso in cui deve essere eseguito il rendering. Se non è ancora stato eseguito il rendering di un esempio con timestamp inferiore all'ora corrente del flusso, è in ritardo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




