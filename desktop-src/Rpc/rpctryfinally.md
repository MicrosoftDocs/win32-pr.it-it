---
title: RpcTryFinally (RPC. h)
description: L'istruzione RpcTryFinally fornisce la gestione strutturata della terminazione.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477506"
---
# <a name="rpctryfinally"></a>RpcTryFinally

L'istruzione **RpcTryFinally** fornisce la gestione strutturata della terminazione. Si verifica un'eccezione durante le istruzioni di esecuzione del blocco di codice associato all'istruzione **RpcTryFinally** , le istruzioni nel blocco di codice associate all'istruzione [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) vengono eseguite. Tutte le istruzioni **RpcTryFinally** devono terminare con un'istruzione [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .

Per ulteriori informazioni, vedere [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

