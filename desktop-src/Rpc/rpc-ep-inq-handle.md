---
title: RPC_EP_INQ_HANDLE (Rpcasync.h)
description: Il tipo \_ di dati \_ RPC EP INQ \_ HANDLE dichiara un handle per un contesto di richiesta. Le applicazioni RPC lo usano per visualizzare le informazioni sull'indirizzo del server archiviate nella mappa degli endpoint.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a401f06077c2f636f679a7733dc7ed99abbdbb5e6b9959998b1f8234b0e4adfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926494"
---
# <a name="rpc_ep_inq_handle"></a>RPC \_ EP \_ INQ \_ HANDLE

Il **tipo di dati RPC \_ \_ EP INQ \_ HANDLE** dichiara un handle per un contesto di richiesta. Le applicazioni RPC lo usano per visualizzare le informazioni sull'indirizzo del server archiviate nella mappa degli endpoint.


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Rpcasync.h (includere Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





