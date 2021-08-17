---
title: RpcTryExcept (Rpc.h)
description: L'istruzione RpcTryExcept fornisce una gestione strutturata delle eccezioni per le applicazioni RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925968"
---
# <a name="rpctryexcept"></a>RpcTryExcept

**L'istruzione RpcTryExcept** fornisce una gestione strutturata delle eccezioni per le applicazioni RPC. Se una delle istruzioni del programma in **RpcTryExcept** genera un'eccezione, vengono eseguite le istruzioni nel blocco di codice [**RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) Tutte **le istruzioni RpcTryExcept** devono essere terminate dall'istruzione [**RpcEndExcept.**](/previous-versions/aa375629(v=vs.80))

Per altre informazioni, vedere [**RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)

**Windows Vista e** versioni successive di Windows:[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) è consigliato per la gestione strutturata delle eccezioni per le eccezioni più comuni come alternativa ai filtri personalizzati con [**RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

