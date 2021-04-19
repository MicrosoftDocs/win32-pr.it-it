---
description: 'Il metodo GetCurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Metodo CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329374"
---
# <a name="cpospassthrugetcurrentposition-method"></a>CPosPassThru. GetCurrentPosition, metodo

Il `GetCurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione corrente, in unità del formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il metodo non è supportato.<br/>   |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null** .<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il metodo [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) per recuperare la posizione più recente. Se **GetMediaTime** ha esito negativo, il metodo chiama **IMediaSeeking:: getCurrentPosition** sul pin connesso.

Il metodo **GetMediaTime** ha esito negativo per impostazione predefinita nella classe di base. Se il filtro memorizza nella cache la posizione corrente, eseguire l'override di **GetMediaTime** per restituire il valore memorizzato nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




