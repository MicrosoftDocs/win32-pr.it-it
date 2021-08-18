---
description: Il Connessione completa una connessione al pin di output.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: CPullPin. Connessione metodo (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37240be1b732410d1e91974922f8ed7dc464b57b2596faa381c646a7513daf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073505"
---
# <a name="cpullpinconnect-method"></a>CPullPin. Connessione metodo

Il `Connect` metodo completa una connessione al pin di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore **all'interfaccia IUnknown** del pin di output.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del pin di input oppure **NULL.**

</dd> <dt>

*bSync* 
</dt> <dd>

Valore booleano che specifica se usare le operazioni di lettura sincrona. Se **TRUE,** il pin esegue operazioni di lettura sincrone sul pin di output. Se **FALSE,** il pin effettua richieste di lettura asincrone.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                               | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione completata.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ GIÀ \_ CONNESSO**</dt> </dl> | Il pin di input è già connesso.<br/>                                  |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>             | Il pin di output non espone [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo durante il processo di connessione del pin di input. Se il metodo ha esito negativo, il pin dovrebbe non riuscire la connessione.

Questo metodo esegue una query sul pin di output per **l'interfaccia IAsyncReader.** Se ha esito positivo, chiama [**CPullPin::D ecideAllocator**](cpullpin-decideallocator.md) per negoziare l'allocatore per la connessione. Se il pin di input ha un allocatore preferito, specificarlo nel *parametro pAlloc.* Il **metodo DecideAllocator** passa questo puntatore al metodo [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del pin di output. In caso contrario, *impostare pAlloc* su **NULL.**

Se il valore di *bSync* è **TRUE,** l'oggetto **CPullPin** effettua richieste di lettura sincrone chiamando [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)del pin di output. In caso contrario, chiama il [**metodo IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) per effettuare richieste di lettura sovrapposte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




