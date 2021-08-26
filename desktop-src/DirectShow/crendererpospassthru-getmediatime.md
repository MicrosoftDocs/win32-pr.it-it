---
description: "Metodo CRendererPosPassThru.GetMediaTime: il metodo GetMediaTime recupera i timestamp nell'esempio corrente."
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Metodo CRendererPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3b8eb4bdd9426d589476265133234bdf3c2d5cfc691bfaced743cc4e75769c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084121"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Metodo CRendererPosPassThru.GetMediaTime

Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStartTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di inizio, in unità del formato di ora corrente.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di fine, in unità del formato di ora corrente. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La conversione in questo formato non è supportata.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>    | Argomento del puntatore **NULL.**<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CPosPassThru::GetMediaTime.**](cpospassthru-getmediatime.md) I valori del timestamp vengono convertiti nel formato di ora corrente chiamando il [**metodo CPosPassThru::ConvertTimeFormat.**](cpospassthru-converttimeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




