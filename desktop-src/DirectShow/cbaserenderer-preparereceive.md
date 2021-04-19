---
description: Il metodo PrepareReceive prepara il filtro per il rendering di un campione.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Metodo CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333342"
---
# <a name="cbaserendererpreparereceive-method"></a>CBaseRenderer. PrepareReceive, metodo

Il `PrepareReceive` metodo prepara il filtro per il rendering di un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT PrepareReceive(
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

Restituisce un valore **HRESULT** . I valori possibili includono quelli nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                        |
| <dl> <dt>**E \_ non riescono**</dt> </dl>                  | non riuscito.<br/>                         |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>            | Errore imprevisto.<br/>               |
| <dl> <dt>**esempio di VFW \_ E \_ \_ rifiutato**</dt> </dl> | Il filtro sta eliminando l'esempio.<br/> |



 

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo dall'interno del metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) , prima di eseguire il rendering di un campione. Se il filtro è in esecuzione, questo metodo pianifica l'esempio per il rendering.

Se il filtro dispone già di un campione in sospeso o se è già stata raggiunta la fine del flusso, il metodo restituisce E \_ imprevisto. Probabilmente il filtro upstream non sta serializzando correttamente le chiamate di streaming.

Se l'algoritmo di pianificazione determina che l'esempio deve essere eliminato (vedere [**CBaseRenderer:: ScheduleSample**](cbaserenderer-schedulesample.md)), il metodo restituisce l' \_ esempio VFW E \_ \_ rifiutato. Tuttavia, il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN di input non passa questo codice di errore al filtro upstream, perché l'eliminazione di un campione non è un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




