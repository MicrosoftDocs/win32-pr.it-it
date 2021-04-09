---
title: Costanti delle opzioni di binding (rpcdce. h)
description: Le applicazioni impostano le costanti dell'opzione di associazione per controllare il modo in cui la libreria di runtime RPC elabora le chiamate a procedure remote. Nella tabella seguente sono elencate tutte le proprietà di binding e i valori costanti rilevanti per le proprietà di associazione.
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
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963996"
---
# <a name="binding-option-constants"></a>Costanti delle opzioni di associazione

Le applicazioni impostano le costanti dell'opzione di associazione per controllare il modo in cui la libreria di runtime RPC elabora le chiamate a procedure remote. Nella tabella seguente sono elencate tutte le proprietà di binding e i valori costanti rilevanti per le proprietà di associazione.

> [!Note]  
> Tutte le opzioni della coda di messaggi (MQ) nella tabella seguente sono valide solo per Windows 2000. Windows XP e versioni successive non supportano l'Accodamento messaggi. Gli sviluppatori sono sconsigliati per l'utilizzo di Accodamento messaggi.

 



| Costante/valore                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ opz \_ binding non \_ causale**</dt> <dt>9</dt> </dl>     | Valore predefinito. Se **false**, l'ordinamento delle chiamate causali. Le chiamate RPC vengono eseguite in un ordine di invio rigoroso. Vedere la sezione Osservazioni.<br/> Se **true**, ordinamento delle chiamate non causale. Le chiamate RPC vengono eseguite in modo indipendente. Vedere la sezione Osservazioni.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ \_ \_ \_ Opzioni C opt max**</dt> <dt>17</dt> </dl>                      | Non necessario per i programmi applicativi. Utilizzato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ dont \_ Fail**</dt> <dt>4</dt> </dl>                                          | Non necessario per i programmi applicativi. Utilizzato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ \_ \_ \_ ID sessione C opt**</dt> <dt>6</dt> </dl>                          | Se **true**, viene generato un ID di sessione per ogni connessione.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ \_Autenticazione a \_ cookie \_**</dt> <dt>7</dt> di C </dl>                       | Se **true**, viene utilizzata l'autenticazione basata su cookie sul lato client per le connessioni. Un puntatore alla struttura [**del \_ \_ \_ \_ \_ descrittore di autenticazione del cookie con consenso esplicito di RPC C**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) viene passato come parametro *OptionValue* in [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ \_Tipo di \_ risorsa opz C \_ \_ UUID**</dt> <dt>8</dt> </dl> | Non necessario per i programmi applicativi. Utilizzato internamente da Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ opt \_ dont \_ indugio**</dt> <dt>13</dt> </dl>                      | Se **true**, forza l'arresto dell'associazione dopo che è stato liberato l'ultimo handle di binding/contesto.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ opz \_ \_ Binding univoco**</dt> <dt>11</dt> </dl>             | Se impostato su **true**, RPC non riutilizza le connessioni esistenti. Viene aperto un handle di binding univoco per ogni connessione e lo stato viene mantenuto per ogni handle di associazione univoco.<br/>                                                                                                               |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, la libreria di runtime RPC esegue le chiamate su un handle di associazione specificato da ogni thread di un'applicazione in un ordine di invio rigoroso. Ciò non garantisce che vengano serializzate le chiamate provenienti da thread diversi nello stesso handle di associazione. Le applicazioni multithreading devono serializzare le chiamate RPC. Se questo comportamento è troppo restrittivo, è possibile abilitare l'ordinamento non causale. Quando si esegue questa operazione, la libreria run-time RPC esegue le chiamate in modo indipendente. Non impone alcun ordine di invio.

Un esempio di applicazione che potrebbe risultare utile per l'ordinamento non causale è un programma multithread i cui thread effettuano chiamate sullo stesso handle di associazione. Analogamente, un programma che utilizza più chiamate asincrone su un handle di associazione troverà un'opzione utile per l'ordinamento non causale. Un altro esempio potrebbe essere un programma proxy Internet che usa un singolo thread per gestire le richieste per più client. In ognuno di questi casi, sarebbe estremamente restrittivo tentare di serializzare le chiamate di procedura remota.

È possibile impostare l'opzione **RPC \_ C \_ opt \_ dont \_ Linger** solo sugli handle di associazione che usano le sequenze di protocollo **ncalrpc** o **ncacn \_ \** _. Non può essere usato nelle sequenze del protocollo _*ncadg \_ \**_ . La funzione [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con questa opzione deve essere chiamata su un handle di associazione in cui è stata eseguita almeno una chiamata RPC. Se non è stata effettuata alcuna chiamata RPC sull'handle di associazione, viene restituito il **\_ \_ \_ tipo \_ di \_ binding non corretto di RPC** dalla chiamata di funzione **RpcBindingSetOption** . L'opzione viene applicata all'intera associazione, indipendentemente dal numero di handle di associazione associati all'associazione. Poiché viene verificata prima che l'associazione venga distrutta, può essere impostata in qualsiasi momento prima della chiusura dell'handle di associazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                 |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h; </dt> <dt>Rpcdcep. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Gestione dei set di connessioni di rete (associazioni)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





