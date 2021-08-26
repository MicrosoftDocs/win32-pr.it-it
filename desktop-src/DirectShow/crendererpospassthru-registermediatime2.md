---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente. Questo metodo usa i *parametri StartTime* *ed EndTime.*
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Metodo CRendererPosPassThru.RegisterMediaTime (Ctlutil.h) - Parametri StartTime ed EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 944d78af6247e7237040f0260a51203a13ef506db36856cfb554d0f2982c0d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084111"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Metodo CRendererPosPassThru.RegisterMediaTime (Ctlutil.h) - Parametri StartTime ed EndTime

Il [**metodo RegisterMediaTime**](crendererpospassthru-registermediatime.md) memorizza nella cache i timestamp dell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* 
</dt> <dd>

Ora di inizio del campione, in unità di 100 nanosecondi.

</dd> <dt>

*EndTime* 
</dt> <dd>

Ora di fine del campione, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operazione completata.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo archivia i valori del timestamp specificati in *StartTime* ed *EndTime.* Il [**metodo CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.

Il filtro deve chiamare questo metodo per ogni esempio ricevuto. Il metodo viene sottoposto a overload per accettare un puntatore all'esempio o i valori del timestamp stessi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Ctlutil.h (includere Flussi.h)                                                                                   |
| Libreria | Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |



 

 




