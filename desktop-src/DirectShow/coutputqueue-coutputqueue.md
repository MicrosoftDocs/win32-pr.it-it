---
description: Metodo del costruttore.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Costruttore COutputQueue. COutputQueue (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330212"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Costruttore COutputQueue. COutputQueue

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInputPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input. L'oggetto fornirà esempi a questo pin.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a un codice restituito **HRESULT** . Impostare il valore su S \_ OK prima di chiamare questo metodo. Al ritorno, *PHR* riceve un valore che indica l'esito positivo o negativo del metodo.

</dd> <dt>

*bAuto* 
</dt> <dd>

Flag che specifica se l'oggetto decide quando creare una coda. Se **true**, l'oggetto crea una coda solo se il pin di input potrebbe bloccarsi. Se **false**, il parametro *bQueue* specifica se creare una coda.

</dd> <dt>

*bQueue* 
</dt> <dd>

Se *bAuto* è **true**, questo parametro viene ignorato. Se *bAuto* è **false**, questo flag specifica se creare una coda.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Numero massimo di campioni da recapitare in un unico batch.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Flag che specifica se utilizzare le dimensioni esatte dei batch. Se **true**, l'oggetto attende gli esempi di *lBatchSize* prima di distribuirli al pin di input. Se **false**, l'oggetto recapita gli esempi mentre li riceve.

</dd> <dt>

*lListSize* 
</dt> <dd>

Dimensioni della cache per la coda. Il valore predefinito, DEFAULTCACHE, è una costante definita per la classe [**CBaseList**](cbaselist.md) .

</dd> <dt>

*dwPriority* 
</dt> <dd>

Priorità del thread che fornisce esempi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *bAuto* è **true**, l'oggetto chiama il metodo [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) sul pin downstream. Se **ReceiveCanBlock** restituisce \_ OK (ovvero il PIN potrebbe bloccarsi in [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Calls), l'oggetto crea un thread per la distribuzione degli esempi. In caso contrario, non crea un thread.

Se *bAuto* è **false**, il valore di *bQueue* determina se creare un thread.

Se l'oggetto crea un thread, assegna l'handle del thread alla variabile membro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) . La routine thread è [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)e il parametro thread è un puntatore a questo. L'oggetto crea anche una coda per contenere gli esempi, fornita dalla variabile membro dell' [**\_ elenco COutputQueue:: m**](coutputqueue-m-list.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




