---
title: RpcTryExcept (RPC. h)
description: L'istruzione RpcTryExcept fornisce la gestione strutturata delle eccezioni per le applicazioni RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RPC RpcTryExcept
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
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120235"
---
# <a name="rpctryexcept"></a>RpcTryExcept

L'istruzione **RpcTryExcept** fornisce la gestione strutturata delle eccezioni per le applicazioni RPC. Se una qualsiasi delle istruzioni Program in **RpcTryExcept** genera un'eccezione, vengono eseguite le istruzioni nel blocco di codice [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Tutte le istruzioni **RpcTryExcept** devono terminare con l'istruzione [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .

Per ulteriori informazioni, vedere [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista e versioni successive di Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) è consigliato per la gestione delle eccezioni strutturata per le eccezioni più comuni come alternativa ai filtri personalizzati con [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

