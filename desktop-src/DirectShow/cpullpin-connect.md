---
description: Il metodo Connect completa una connessione al pin di output.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Metodo CPullPin. Connect (Pullpin. h)
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
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331181"
---
# <a name="cpullpinconnect-method"></a>Metodo CPullPin. Connect

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

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** del PIN di output.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del PIN di input o **null**.

</dd> <dt>

*bSync* 
</dt> <dd>

Valore booleano che specifica se utilizzare le letture sincrone. Se **true**, il pin esegue operazioni di lettura sincrone sul pin di output. Se **false**, il pin esegue richieste di lettura asincrone.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT**. Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                               | Descrizione                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                      | Esito positivo.<br/>                                                             |
| <dl> <dt>**VFW \_ E \_ già \_ connesso**</dt> </dl> | Il pin di input è già connesso.<br/>                                  |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | Il pin di output non espone [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo durante il processo di connessione del PIN di input. Se il metodo ha esito negativo, il PIN dovrebbe interrompere la connessione.

Questo metodo esegue una query sul pin di output per l'interfaccia **IAsyncReader** . Se ha esito positivo, viene chiamato [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) per negoziare l'allocatore per la connessione. Se il pin di input ha un allocatore preferito, specificarlo nel parametro *pAlloc* . il metodo **DecideAllocator** passa questo puntatore al metodo [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del PIN di output. In caso contrario, impostare *pAlloc* su **null**.

Se il valore di *bSync* è **true**, l'oggetto **CPullPin** esegue richieste di lettura sincrone, chiamando il pin di output [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned). In caso contrario, chiama il metodo [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) per eseguire richieste di lettura sovrapposte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




