---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente. Questo metodo usa i parametri *StartTime* e *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parametri StartTime e EndTime
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
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334341"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a>Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)-parametri StartTime e EndTime

Il metodo [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) memorizza nella cache i timestamp dell'esempio corrente.

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

Ora di inizio di esempio, in unità di 100 nanosecondi.

</dd> <dt>

*EndTime* 
</dt> <dd>

Ora di fine campione, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Esito positivo.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo archivia i valori timestamp specificati in *StartTime* e *EndTime*. Il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.

Il filtro deve chiamare questo metodo per ogni campione che riceve. Il metodo è sottoposto a overload per accettare un puntatore all'esempio o i valori timestamp stessi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione  | Ctlutil. h (include Streams. h)                                                                                   |
| Libreria | Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |



 

 




