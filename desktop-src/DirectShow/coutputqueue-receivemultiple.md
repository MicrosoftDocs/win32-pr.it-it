---
description: Il metodo ReceiveMultiple recapita un batch di esempi di supporti al pin di input.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Metodo COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324678"
---
# <a name="coutputqueuereceivemultiple-method"></a>COutputQueue. ReceiveMultiple, metodo

Il `ReceiveMultiple` Metodo recapita un batch di campioni multimediali al pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSamples* 
</dt> <dd>

Indirizzo di un puntatore a una matrice di campioni.

</dd> <dt>

*nSamples* 
</dt> <dd>

Numero di campioni nella matrice.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Puntatore a una variabile che riceve il numero di campioni recapitati correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Notifica di fine del flusso ricevuta prima di elaborare l'esempio.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                                           |



 

## <a name="remarks"></a>Commenti

Se l'oggetto utilizza un thread, questo metodo Accoda tutti gli esempi passati nella matrice. In caso contrario, il metodo chiama il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) sul pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




