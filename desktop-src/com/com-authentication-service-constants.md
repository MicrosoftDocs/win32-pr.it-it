---
title: Costanti del servizio di autenticazione (RpcDce.h)
description: Definisce i servizi di autenticazione identificando il pacchetto di sicurezza che fornisce il servizio, ad esempio NTLMSSP, Kerberos o Schannel.
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
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
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14cf6f0ab42b03d028d52df8160cad286e8c37af3988d8ca3b9736dad538012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993781"
---
# <a name="authentication-service-constants"></a>Costanti del servizio di autenticazione

Definisce i servizi di autenticazione identificando il pacchetto di sicurezza che fornisce il servizio, ad esempio NTLMSSP, Kerberos o Schannel.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NONE**</dt> <dt>0</dt> </dl>                              | Nessuna autenticazione.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PRIVATE**</dt> <dt>1</dt> </dl>        | Autenticazione con chiave privata DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DCE \_ PUBLIC**</dt> <dt>2</dt> </dl>           | Autenticazione con chiave pubblica DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEC \_ PUBLIC**</dt> <dt>4</dt> </dl>           | Autenticazione con chiave pubblica DEC. Riservato per utilizzi futuri.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ NEGOTIATE**</dt> <dt>9</dt> </dl>  | Provider di supporto per la sicurezza Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ WINNT**</dt> <dt>10</dt> </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL**</dt> <dt>14</dt> </dl>    | Provider di supporto per la sicurezza Schannel. Questo servizio di autenticazione supporta SSL 2.0, SSL 3.0, TLS e PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ GSS \_ KERBEROS**</dt> <dt>16</dt> </dl>    | Provider di supporto per la sicurezza Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DPA**</dt> <dt>17</dt> </dl>                                | Provider di supporto per la sicurezza DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MSN**</dt> <dt>18</dt> </dl>                                | Provider di supporto per la sicurezza MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ KERNEL \_ AUTHN \_ C**</dt> <dt>20</dt> </dl>                       | Provider di supporto per la sicurezza del kernel.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DIGEST**</dt> <dt>21</dt> </dl>                       | Provider di supporto per la sicurezza digest.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ NEGO \_ EXTENDER**</dt> <dt>30</dt> </dl> | Provider di supporto per la sicurezza neGO Extender.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Provider di supporto per la sicurezza PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ MQ**</dt> <dt>100</dt> </dl>                                  | Provider di supporto per la sicurezza MQ.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ C \_ AUTHN \_ DEFAULT**</dt> <dt>0xFFFFFFFFL</dt> </dl>           | Servizio di autenticazione predefinito del sistema. Quando questo valore viene specificato, COM utilizza il normale algoritmo di negoziazione di negoziazione di sicurezza per selezionare un servizio di autenticazione. Per altre informazioni, vedere [Negoziazione di negoziazione della negoziazione della sicurezza.](security-blanket-negotiation.md) <br/> |



## <a name="remarks"></a>Commenti

Queste costanti vengono usate nelle strutture [**SOLE \_ AUTHENTICATION \_ SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) e [**SOLE AUTHENTICATION \_ \_ INFO.**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) La **struttura SOLE AUTHENTICATION \_ \_ SERVICE** viene passata dal server alla [**funzione CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e può essere recuperata dalla [**funzione CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) Un puntatore a una **struttura \_ SOLE AUTHENTICATION \_ INFO** viene passato dal client a **CoInitializeSecurity.** Per altre informazioni sui pacchetti di sicurezza identificati da questi valori, ad esempio NTLMSSP e Kerberos, vedere [Com and Security Packages](com-and-security-packages.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Coinitializesecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**SOLE \_ INFORMAZIONI DI \_ AUTENTICAZIONE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**UNICO \_ SERVIZIO DI \_ AUTENTICAZIONE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

