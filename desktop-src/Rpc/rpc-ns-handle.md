---
title: RPC_NS_HANDLE (rpcnsi. h)
description: Il tipo di dati \_ handle NS RPC \_ definisce un handle del servizio nome.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518718"
---
# <a name="rpc_ns_handle"></a>\_handle NS \_ RPC

Il tipo di **dati \_ \_ handle NS RPC** definisce un handle del servizio nome.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Commenti

Un handle del servizio nome è una variabile opaca che contiene informazioni utilizzate dalla libreria di runtime RPC per restituire i dati RPC seguenti dal nome del database del servizio:

-   Handle di associazione server
-   UUID delle risorse offerte dai membri del profilo del server
-   Membri gruppo

L'ambito di un handle del servizio Name è da una routine "Begin" tramite la routine "Done" corrispondente.

Le applicazioni sono responsabili del controllo della concorrenza degli handle del servizio nome nei thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcnsi. h (include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





