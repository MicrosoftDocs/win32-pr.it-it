---
title: Costanti di timeout di binding (rpcdce. h)
description: La libreria RPC utilizza le costanti di timeout dell'associazione per specificare la quantità relativa di tempo che deve trascorrere per stabilire un'associazione al server prima di rinunciare.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301351"
---
# <a name="binding-time-out-constants"></a>Costanti di timeout di binding

La libreria RPC utilizza le costanti di timeout dell'associazione per specificare la quantità relativa di tempo che deve trascorrere per stabilire un'associazione al server prima di rinunciare. Il timeout può essere abilitato con una chiamata alla funzione [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) . L'elenco seguente contiene i valori di timeout validi.



| Costante/valore                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Timeout di binding C infinito**</dt> <dt> 10</dt> </dl> | Continua a tentare di stabilire le comunicazioni per sempre.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Timeout binding C minimo**</dt> <dt>0</dt> </dl>                   | Tenta la quantità minima di tempo per il protocollo di rete utilizzato. Questo valore predilige il tempo di risposta rispetto alla correttezza per determinare se il server è in esecuzione.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Timeout predefinito associazione C**</dt> <dt>5</dt> </dl>       | Tenta un periodo di tempo medio per l'utilizzo del protocollo di rete. Questo valore fornisce la correttezza per determinare se un server è in esecuzione e restituisce il peso del tempo di risposta uguale. Si tratta del valore predefinito.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ Timeout max binding C**</dt> <dt>9</dt> </dl>                   | Tenta la quantità di tempo più lungo per il protocollo di rete utilizzato. Questo valore predilige la correttezza per determinare se un server viene eseguito nel tempo di risposta.<br/>                                            |



## <a name="remarks"></a>Commenti

I valori nella tabella precedente non sono in secondi. Questi valori rappresentano una quantità di tempo relativa su una scala da zero a 10. Per altre informazioni su come evitare i ritardi di comunicazione, vedere impedire blocchi lato client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





