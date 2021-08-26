---
description: Il metodo GetCurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaSeeking::GetCurrentPosition.
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Metodo CPosPassThru.GetCurrentPosition (Ctlutil.h)
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
ms.openlocfilehash: a43477d019639b4e1de5c2aa40f18c99f7b902498c671f8106d5832c43b11584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084161"
---
# <a name="cpospassthrugetcurrentposition-method"></a>Metodo CPosPassThru.GetCurrentPosition

Il `GetCurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il [**metodo IMediaSeeking::GetCurrentPosition.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition)

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

Puntatore a una variabile che riceve la posizione corrente, in unità del formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il metodo non è supportato.<br/>   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo chiama il [**metodo CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) per recuperare la posizione più recente. Se **GetMediaTime ha** esito negativo, il metodo chiama **IMediaSeeking::GetCurrentPosition** sul pin connesso.

Per impostazione predefinita, il metodo **GetMediaTime** ha esito negativo nella classe di base. Se il filtro memorizza nella cache la posizione corrente, eseguire **l'override di GetMediaTime** per restituire il valore memorizzato nella cache.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




