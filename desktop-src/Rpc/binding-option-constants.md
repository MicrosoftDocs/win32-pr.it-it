---
title: Costanti delle opzioni di associazione (Rpcdce.h)
description: Le applicazioni impostano le costanti delle opzioni di associazione per controllare il modo in cui la libreria di runtime RPC elabora le chiamate di procedura remota. Nella tabella seguente sono elencate le proprietà di associazione e i valori costanti pertinenti per le proprietà di associazione.
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147d36cf66bb3a45add61b8639ccd3fada31856e72fce8c1f96d7a021e1d5e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023121"
---
# <a name="binding-option-constants"></a>Costanti delle opzioni di binding

Le applicazioni impostano le costanti delle opzioni di associazione per controllare il modo in cui la libreria di runtime RPC elabora le chiamate di procedura remota. Nella tabella seguente sono elencate le proprietà di associazione e i valori costanti pertinenti per le proprietà di associazione.

> [!Note]  
> Tutte le opzioni della coda di messaggi nella tabella seguente sono valide solo per Windows 2000. Windows XP e versioni successive non supportano l'accodamento messaggi. Gli sviluppatori sono sconsigliati di usare l'accodamento messaggi.

 



| Costante/valore                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ OPT \_ BINDING \_ NONCAUSAL**</dt> <dt>9</dt> </dl>     | Valore predefinito. Se **FALSE,** ordinamento causale delle chiamate. Le chiamate RPC vengono eseguite in un ordine rigoroso di invio. Vedere la sezione Osservazioni.<br/> Se **TRUE,** ordinamento delle chiamate noncausale. Le chiamate RPC vengono eseguite in modo indipendente. Vedere la sezione Osservazioni.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ C \_ OPT \_ MAX \_ OPTIONS**</dt> <dt>17</dt> </dl>                      | Non necessario per i programmi applicativi. Usato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ DONT \_ FAIL**</dt> <dt>4</dt> </dl>                                          | Non necessario per i programmi applicativi. Usato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C \_ OPT \_ SESSION \_ ID**</dt> <dt>6</dt> </dl>                          | Se **TRUE,** viene generato un ID di sessione per ogni connessione.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C \_ OPT \_ COOKIE \_ AUTH**</dt> <dt>7</dt> </dl>                       | Se **TRUE,** per le connessioni viene usata l'autenticazione basata su cookie sul lato client. Un puntatore alla [**struttura RPC C OPT COOKIE \_ \_ \_ \_ \_ AUTH DESCRIPTOR**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) viene passato come *parametro OptionValue* in [**RpcBindingSetOption.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ C \_ OPT RESOURCE TYPE \_ \_ \_ UUID**</dt> <dt>8</dt> </dl> | Non necessario per i programmi applicativi. Usato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ DONT \_ LINGER**</dt> <dt>13</dt> </dl>                      | Se **TRUE,** forza l'arresto forzato dell'associazione dopo che l'ultimo handle di associazione/handle di contesto è stato liberato.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ OPT \_ UNIQUE \_ BINDING**</dt> <dt>11</dt> </dl>             | Se impostato su **true,** RPC non riutilizza le connessioni esistenti. Viene aperto un handle di associazione univoco per ogni connessione e lo stato viene mantenuto per ogni handle di associazione univoco.<br/>                                                                                                               |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, la libreria di runtime RPC esegue le chiamate su un determinato handle di associazione da ogni thread di un'applicazione in un ordine di invio rigoroso. Ciò non garantisce che le chiamate da thread diversi sullo stesso handle di associazione siano serializzate. Le applicazioni multithreading devono serializzare le chiamate RPC. Se questo comportamento è troppo restrittivo, è possibile abilitare l'ordinamento noncausale. In questo caso, la libreria di runtime RPC esegue le chiamate in modo indipendente. Non impone alcun ordinamento per l'invio.

Un esempio di applicazione che potrebbe trovare utile l'ordinamento noncausale è un programma multithreading i cui thread effettuano chiamate sullo stesso handle di associazione. Analogamente, un programma che usa più chiamate asincrone su un handle di associazione troverà un'opzione utile per l'ordinamento noncausale. Un altro esempio potrebbe essere un programma proxy Internet che usa un singolo thread per gestire le richieste per più client. In ognuno di questi casi, sarebbe estremamente restrittivo provare a serializzare le chiamate di procedura remota.

**L'opzione RPC C OPT \_ \_ \_ DONT \_ LINGER** può essere impostata solo su handle di associazione che usano le sequenze di protocollo **ncalrpc** o **ncacn \_ \** _. Non può essere usato nelle _*sequenze di protocollo ncadg. \_ \**_ La [funzione _ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con questa opzione deve essere chiamata su un handle di associazione in cui è stata effettuata almeno una chiamata RPC. Se non è stata effettuata alcuna chiamata RPC sull'handle di associazione, **RPC S WRONG KIND OF \_ \_ \_ \_ \_ BINDING** viene restituito dalla chiamata di funzione **RpcBindingSetOption.** L'opzione ha effetto per l'intera associazione, indipendentemente dal numero di handle di associazione associati all'associazione. Poiché viene controllata prima dell'eliminazione, l'associazione può essere impostata in qualsiasi momento prima della chiusura dell'handle di associazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                 |
| Intestazione<br/>                   | <dl> <dt>Rpcdce.h; </dt> <dt>Rpcdcep.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Gestione dei set di connessioni di rete (associazioni)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





