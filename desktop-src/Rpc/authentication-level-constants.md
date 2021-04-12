---
title: Costanti Authentication-Level (rpcdce. h)
description: Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a varie funzioni di run-time.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518729"
---
# <a name="authentication-level-constants"></a>Costanti a livello di autenticazione

Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a varie funzioni di run-time. Questi livelli sono elencati per aumentare l'autenticazione. Ogni nuovo livello aggiunge l'autenticazione fornita dal livello precedente. Se la libreria di runtime RPC non supporta il livello specificato, viene automaticamente aggiornata al livello superiore supportato successivo.



| Costante                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**\_ \_ \_ valore predefinito del livello auth C RPC \_**</dt> </dl>                    | Utilizza il livello di autenticazione predefinito per il servizio di autenticazione specificato.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**\_ \_ livello auth C \_ RPC \_**</dt> </dl>                             | Non esegue alcuna autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**\_connessione a \_ livello auth \_ C \_ RPC**</dt> </dl>                    | L'autenticazione viene eseguita solo quando il client stabilisce una relazione con un server.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**\_chiamata al \_ livello auth \_ C \_ RPC**</dt> </dl>                             | Esegue l'autenticazione solo all'inizio di ogni chiamata di procedura remota quando il server riceve la richiesta. Non si applica alle chiamate a procedure remote effettuate utilizzando le sequenze di protocollo basate sulla connessione (quelle che iniziano con il prefisso "ncacn"). Se la sequenza di protocollo in un handle di associazione è una sequenza di protocollo basata sulla connessione e si specifica questo livello, questa routine utilizzerà invece la \_ \_ costante PKT del livello auth C RPC \_ \_ .<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**\_ \_ \_ PKT livello auth C RPC \_**</dt> </dl>                                | Autentica solo che tutti i dati ricevuti sono dal client previsto. Non convalida i dati stessi.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**\_ \_ \_ integrità PKT del livello auth \_ C \_ RPC**</dt> </dl> | Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**\_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_**</dt> </dl>       | Include tutti i livelli precedenti e garantisce che i dati di testo non crittografati possano essere visualizzati solo dal mittente e dal destinatario. Nel caso locale, ciò comporta l'uso di un canale sicuro. Nel caso remoto, questo implica la crittografia del valore dell'argomento di ogni chiamata di procedura remota.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Commenti

Indipendentemente dal valore specificato dalla costante, **ncalrpc** usa sempre la \_ \_ \_ privacy PKT del livello auth C di RPC \_ \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





