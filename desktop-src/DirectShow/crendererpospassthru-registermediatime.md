---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
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
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327201"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Metodo CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)

Il metodo **RegisterMediaTime** memorizza nella cache i timestamp dell'esempio corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>                        |
| <dl> <dt>**\_ \_ tempo medio E \_ \_ non \_ impostato per VFW**</dt> </dl> | Per l'esempio non è indicato il timestamp.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo archivia i timestamp dell'esempio corrente. Il metodo [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.

Il filtro deve chiamare questo metodo per ogni campione che riceve. Il metodo è sottoposto a overload per accettare un puntatore all'esempio o i valori timestamp stessi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




