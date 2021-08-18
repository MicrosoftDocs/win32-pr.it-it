---
title: Costanti di timeout dell'associazione (Rpcdce.h)
description: La libreria RPC usa le costanti di timeout dell'associazione per specificare la quantità di tempo relativa da impiegare per stabilire un'associazione al server prima di rinunciare.
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
ms.openlocfilehash: 125a38dd41445ba0661d13c61e7c79e689bc29abffa535791b233c40cfb704ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932362"
---
# <a name="binding-time-out-constants"></a>Costanti di timeout dell'associazione

La libreria RPC usa le costanti di timeout dell'associazione per specificare la quantità di tempo relativa da impiegare per stabilire un'associazione al server prima di rinunciare. Il timeout può essere abilitato con una chiamata alla [**funzione RpcMgmtSetComTimeout.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) L'elenco seguente contiene i valori di timeout validi.



| Costante/valore                                                                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ INFINITE \_ TIMEOUT**</dt> <dt> 10</dt> </dl> | Continua a tentare di stabilire comunicazioni per sempre.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ MIN \_ TIMEOUT**</dt> <dt>0</dt> </dl>                   | Prova la quantità minima di tempo per il protocollo di rete in uso. Questo valore favorisce il tempo di risposta rispetto alla correttezza per determinare se il server è in esecuzione.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ DEFAULT \_ TIMEOUT**</dt> <dt>5</dt> </dl>       | Prova una quantità media di tempo per il protocollo di rete in uso. Questo valore fornisce la correttezza per determinare se un server è in esecuzione e assegna al tempo di risposta lo stesso peso. Si tratta del valore predefinito.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ MAX \_ TIMEOUT**</dt> <dt>9</dt> </dl>                   | Prova la quantità di tempo più lunga per il protocollo di rete in uso. Questo valore favorisce la correttezza nel determinare se un server è in esecuzione nel tempo di risposta.<br/>                                            |



## <a name="remarks"></a>Commenti

I valori nella tabella precedente non sono in secondi. Questi valori rappresentano una quantità di tempo relativa su una scala da zero a 10. Per altre informazioni su come evitare ritardi di comunicazione, vedere Prevenzione dei blocchi sul lato client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





