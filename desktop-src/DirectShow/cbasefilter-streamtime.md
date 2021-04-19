---
description: Il metodo StreamTime recupera l'ora del flusso corrente.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Metodo CBaseFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331654"
---
# <a name="cbasefilterstreamtime-method"></a>CBaseFilter. StreamTime, metodo

Il metodo **StreamTime** recupera l'ora del flusso corrente.

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

Riferimento a un oggetto [**CRefTime**](creftime.md) che riceve l'ora del flusso corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                      | Descrizione                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>             | Esito positivo.<br/>                         |
| <dl> <dt>**VFW \_ E \_ nessun \_ Clock**</dt> </dl> | Nessun clock di riferimento disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Il tempo di flusso viene definito come ora di riferimento corrente (come indicato dall'orologio di riferimento) meno l'ora di inizio (specificata da [**CBaseFilter:: m \_ tStart**](cbasefilter-m-tstart.md)). Il *timestamp* di un campione multimediale specifica l'ora del flusso in cui deve essere eseguito il rendering. Se non è ancora stato eseguito il rendering di un campione con un timestamp inferiore al tempo di flusso corrente, è in ritardo.

Questo metodo ottiene l'ora del flusso chiamando [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) per ottenere l'ora di riferimento corrente e quindi sottraendo l'ora di inizio iniziale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




