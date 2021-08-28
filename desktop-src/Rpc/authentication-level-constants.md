---
title: Authentication-Level costanti (Rpcdce.h)
description: Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a diverse funzioni di run-time.
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
ms.openlocfilehash: 03c27fa63a437c3c8a93c3d2e5e1f1983e341d5709e986c83459a3f505b46c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080921"
---
# <a name="authentication-level-constants"></a>Costanti a livello di autenticazione

Le costanti a livello di autenticazione rappresentano i livelli di autenticazione passati a diverse funzioni di run-time. Questi livelli sono elencati in ordine di autenticazione crescente. Ogni nuovo livello aggiunge all'autenticazione fornita dal livello precedente. Se la libreria di runtime RPC non supporta il livello specificato, viene aggiornato automaticamente al livello supportato superiore successivo.



| Costante                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA A LIVELLO DI AUTENTICAZIONE \_ RPC C \_ \_ \_**</dt> </dl>                    | Utilizza il livello di autenticazione predefinito per il servizio di autenticazione specificato.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ NONE**</dt> </dl>                             | Non esegue alcuna autenticazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT**</dt> </dl>                    | L'autenticazione viene eseguita solo quando il client stabilisce una relazione con un server.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**CHIAMATA \_ A LIVELLO DI AUTENTICAZIONE RPC C \_ \_ \_**</dt> </dl>                             | Esegue l'autenticazione solo all'inizio di ogni chiamata di procedura remota quando il server riceve la richiesta. Non si applica alle chiamate di procedura remota effettuate utilizzando le sequenze di protocollo basate sulla connessione (quelle che iniziano con il prefisso "ncacn"). Se la sequenza di protocollo in un handle di associazione è una sequenza di protocollo basata sulla connessione e si specifica questo livello, questa routine usa invece la costante \_ PKT RPC C \_ AUTHN \_ \_ LEVEL.<br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT**</dt> </dl>                                | Autentica solo che tutti i dati ricevuti sono provenienti dal client previsto. Non convalida i dati stessi.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**INTEGRITÀ PKT A \_ \_ LIVELLO DI \_ \_ AUTENTICAZIONE \_ RPC C**</dt> </dl> | Autentica e verifica che nessuno dei dati trasferiti tra client e server sia stato modificato.<br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**</dt> </dl>       | Include tutti i livelli precedenti e garantisce che i dati non crittografati possano essere visti solo dal mittente e dal destinatario. Nel caso locale, ciò comporta l'uso di un canale sicuro. Nel caso remoto, ciò comporta la crittografia del valore dell'argomento di ogni chiamata di procedura remota.<br/>                                                                                                                                                                 |



## <a name="remarks"></a>Commenti

Indipendentemente dal valore specificato dalla costante , **ncalrpc** usa sempre RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



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

 

 





