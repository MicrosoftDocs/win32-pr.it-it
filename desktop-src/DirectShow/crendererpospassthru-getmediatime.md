---
description: Il metodo GetMediaTime recupera i timestamp nell'esempio corrente.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Metodo CRendererPosPassThru. GetMediaTime (Ctlutil. h)
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
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330205"
---
# <a name="crendererpospassthrugetmediatime-method"></a>CRendererPosPassThru. GetMediaTime, metodo

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

Puntatore a una variabile che riceve l'ora di inizio, in unità del formato dell'ora corrente.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora di fine, in unità del formato dell'ora corrente. Può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La conversione in questo formato non è supportata.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/>                  |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) . I valori dell'indicatore di data e ora vengono convertiti nel formato di ora corrente chiamando il metodo [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




