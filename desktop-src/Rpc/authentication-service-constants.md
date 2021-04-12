---
title: Costanti Authentication-Service (rpcdce. h)
description: Le costanti del servizio di autenticazione rappresentano i servizi di autenticazione passati a varie funzioni di run-time.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518724"
---
# <a name="authentication-service-constants"></a>Costanti Authentication-Service

Le costanti del servizio di autenticazione rappresentano i servizi di autenticazione passati a varie funzioni di run-time.

Le costanti seguenti sono valori validi per il parametro *AuthnSvc* .



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ \_Autenticazione C \_ Nessuna**</dt> <dt>0</dt> </dl>                              | Nessuna autenticazione.<br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AuthN \_ DCE \_ privato**</dt> <dt>1</dt> </dl>        | Usare l'autenticazione con chiave privata DCE (Distributed Computing Environment).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ Autorità di \_ autenticazione \_ DCE C \_ pubblica**</dt> <dt>2</dt> </dl>           | Autenticazione con chiave pubblica DCE (riservata per uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AuthN \_ dicembre \_ pubblico**</dt> <dt>4</dt> </dl>           | Autenticazione con chiave pubblica DEC (riservata per uso futuro).<br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AuthN \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Utilizzare [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate). Questo SSP negozia tra l'utilizzo dei provider di supporto per la sicurezza (SSP) del protocollo NTLM e Kerberos.<br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ \_ \_ WinNT auth**</dt> <dt>10</dt> di C </dl>                          | Utilizzare il [provider di servizi condivisi di Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).<br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AuthN \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Usare [SSP Schannel](/windows/desktop/SecAuthN/secure-channel). Questo SSP supporta Secure Socket Layer (SSL), la tecnologia di comunicazione privata (PCT) e la sicurezza a livello di trasporto (TLS).<br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ Autenticazione del linguaggio C ( \_ \_ \_ Kerberos**</dt> ) a <dt>16</dt> </dl>    | Utilizzare [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).<br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ \_Autenticazione \_ DPA**</dt> <dt></dt> </dl>                                | Usare l'autenticazione della password distribuita (DPA).<br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ \_MSN AuthN \_ MSN**</dt> <dt>18</dt> </dl>                                | SSP del protocollo di autenticazione usato per la rete Microsoft (MSN).<br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ \_ \_ Digest di autenticazione C**</dt> <dt>21</dt> </dl>                       | Windows XP o versione successiva: usare [SSP Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)<br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ Nego \_ Extender**</dt> <dt>30</dt> di autenticazione C </dl> | Windows 7 o versioni successive: riservato. Non utilizzare<br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AuthN \_ mq**</dt> <dt>100</dt> </dl>                                  | Questo SSP fornisce un wrapper compatibile con SSPI per il protocollo a livello di trasporto di Microsoft Message Queue (MSMQ).<br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ 0xFFFFFFFF \_ \_ predefinito di autenticazione C**</dt> <dt></dt> </dl>            | Usare il servizio di autenticazione predefinito.<br/>                                                                                                                                   |



## <a name="remarks"></a>Commenti

Specificare RPC \_ C \_ AuthN \_ None per disattivare l'autenticazione per le chiamate di procedure remote effettuate su un handle di binding. Quando si specifica l' \_ impostazione predefinita per l'autenticazione RPC c \_ \_ , la libreria di runtime RPC USA \_ il \_ \_ servizio di autenticazione WinNT c AuthN per le chiamate di procedure remote effettuate usando l'handle di associazione.

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

[**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[**RpcBindingInqAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

