---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Il \_ tipo di dati dell'handle di binding RPC dichiara un handle di associazione contenente le informazioni utilizzate dalla libreria di runtime RPC per accedere alle informazioni di binding.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743791"
---
# <a name="rpc_binding_handle"></a>\_handle di binding RPC \_

Il tipo di dati dell' **\_ handle di binding RPC** dichiara un handle di associazione contenente le informazioni utilizzate dalla libreria di runtime RPC per accedere alle informazioni di binding.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Commenti

La libreria di runtime utilizza le informazioni di binding per stabilire una relazione client-server che consente l'esecuzione di chiamate di procedure remote. In base al contesto in cui viene creato un handle di associazione, viene considerato un handle di associazione server o un handle di associazione client.

Un handle di associazione server contiene le informazioni necessarie a un client per stabilire una relazione con un server specifico. Un numero qualsiasi di routine di Runtime API RPC restituisce un handle di associazione server che può essere utilizzato per eseguire una chiamata di procedura remota.

Non è possibile usare un handle di associazione client per eseguire una chiamata di procedura remota. La libreria di runtime RPC crea e fornisce un handle di associazione client a una procedura denominata-Server (detta anche routine Server-Manager) come parametro dell'handle di \_ binding RPC \_ . L'handle di associazione client contiene informazioni sul client chiamante.

Le funzioni ** \* RpcBinding* _ _*e \* RpcNsBinding*_ RESTITUIscono il \_ tipo di associazione RPC del codice di stato \_ errato \_ \_ \_ quando un'applicazione fornisce il tipo di handle di binding errato.

Un'applicazione può condividere un singolo handle di binding tra più thread di esecuzione. La libreria di runtime RPC gestisce le chiamate a procedure remote simultanee che utilizzano un singolo handle di associazione. Tuttavia, l'applicazione è responsabile del controllo della concorrenza dell'handle di associazione per le operazioni che modificano un handle di associazione. Queste operazioni includono le routine seguenti:

-   [_ *RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Se, ad esempio, un'applicazione condivide un handle di associazione tra due thread di esecuzione e Reimposta l'endpoint dell'associazione-handle in uno dei thread chiamando [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), i risultati non sono definiti. È possibile che venga reimpostato anche l'handle dell'associazione sull'altro thread oppure l'operazione potrebbe non riuscire oppure il processo potrebbe arrestarsi in modo anomalo. Un errore comune è quello di liberare un handle di associazione mentre è in corso una chiamata al suo interno. Questo problema in genere blocca il processo chiamante.

Se non si desidera la concorrenza, è possibile progettare un'applicazione per creare una copia di un handle di associazione chiamando [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy). In questo caso, un'operazione al primo handle di associazione non ha alcun effetto sul secondo handle di associazione.

Le routine che richiedono un handle di associazione come parametro mostrano un tipo di dati **dell' \_ \_ handle di binding RPC**. I parametri dell'handle di binding vengono passati per valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h (include RPC. h)</dt> </dl> |



 

 





