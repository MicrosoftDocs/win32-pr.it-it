---
title: Flag di registrazione dell'interfaccia (rpcdce. h)
description: Le costanti seguenti vengono usate nel parametro flags delle funzioni RpcServerRegisterIf2 e RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121118"
---
# <a name="interface-registration-flags"></a>Flag di registrazione dell'interfaccia

Le costanti seguenti vengono usate nel parametro *Flags* delle funzioni [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) e [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td style="text-align: left;">Semantica dell'interfaccia standard.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Quando questo flag di interfaccia viene registrato, il runtime RPC richiama il callback di sicurezza registrato per tutte le chiamate, indipendentemente dall'identità, dalla sequenza di protocollo o dal livello di autenticazione del client.<br/>
<blockquote>
[!Note]<br />
Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1. Quando questo flag non è impostato, RPC filtra automaticamente tutte le chiamate non autenticate prima che raggiungano il callback di sicurezza.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Quando questo flag di interfaccia viene registrato, il runtime RPC rifiuta le chiamate effettuate dai client remoti. Vengono rifiutate anche tutte le chiamate locali che usano le sequenze di protocollo ncadg_ * e ncacn_ *, ad eccezione di ncacn_np. RPC consente ncacn_NP chiamate solo se la chiamata non proviene da SRV. Le chiamate da Ncalrpc vengono sempre elaborate.<br/>
<blockquote>
[!Note]<br />
Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Si tratta di un'interfaccia di <strong>ascolto automatico</strong> . Il tempo di esecuzione inizia ad ascoltare le chiamate non appena viene registrata la prima interfaccia autolisten e interrompe l'ascolto quando viene annullata la registrazione dell'ultima interfaccia Autolist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Riservato per OLE. Non usare questo flag.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">Attualmente non implementato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Limita le connessioni ai client che utilizzano un livello di autorizzazione superiore a RPC_C_AUTHN_LEVEL_NONE. La specifica di questo flag consente ai client di passare alla sessione <strong>null</strong> . In Windows XP e Windows Server 2003 tali client non sono consentiti. I client che non riescono a RPC_IF_ALLOW_SECURE_ONLY test ricevono un errore RPC_S_ACCESS_DENIED. L'utilizzo del flag RPC_IF_ALLOW_SECURE_ONLY non implica né garantisce un livello di privilegio elevato per la parte dell'utente chiamante. RPC verifica solo che l'utente disponga di credenziali valide. l'utente chiamante può usare l'account Guest o altri account con privilegi limitati. Non presupporre privilegi elevati quando viene usato RPC_IF_ALLOW_SECURE_ONLY.<br/> <strong>Windows NT 4,0 e Windows Me/98/95:  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Disabilita la memorizzazione nella cache di callback di sicurezza, forzando un callback di sicurezza per ogni chiamata RPC su una determinata interfaccia.<br/>
<blockquote>
[!Note]<br />
Questo flag è disponibile a partire da Windows XP con SP2 e Windows Server 2003 con SP1.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





