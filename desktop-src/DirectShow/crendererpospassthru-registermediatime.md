---
description: Il metodo RegisterMediaTime memorizza nella cache i timestamp dell'esempio corrente.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Metodo CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)
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
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054381"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Metodo CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)

Il **metodo RegisterMediaTime** memorizza nella cache i timestamp dell'esempio corrente.

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

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                                  | Descrizione                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>                        |
| <dl> <dt>**ORA SUPPORTO VFW \_ E \_ NON \_ \_ \_ IMPOSTATA**</dt> </dl> | L'esempio non è contrassegnato con un timestamp.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo archivia i timestamp dell'esempio corrente. Il [**metodo CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera gli stessi valori.

Il filtro deve chiamare questo metodo per ogni esempio ricevuto. Il metodo viene sottoposto a overload per accettare un puntatore all'esempio o i valori del timestamp stessi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




