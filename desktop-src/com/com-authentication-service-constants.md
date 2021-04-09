---
title: Costanti del servizio di autenticazione (RpcDce. h)
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
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121530"
---
# <a name="authentication-service-constants"></a>Costanti del servizio di autenticazione

Definisce i servizi di autenticazione identificando il pacchetto di sicurezza che fornisce il servizio, ad esempio NTLMSSP, Kerberos o Schannel.



| Costante/valore                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <dt>**RPC \_ \_Autenticazione C \_ Nessuna**</dt> <dt>0</dt> </dl>                              | Nessuna autenticazione.<br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <dt>**RPC \_ C \_ AuthN \_ DCE \_ privato**</dt> <dt>1</dt> </dl>        | Autenticazione con chiave privata DCE.<br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <dt>**RPC \_ Autorità di \_ autenticazione \_ DCE C \_ pubblica**</dt> <dt>2</dt> </dl>           | Autenticazione con chiave pubblica DCE.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <dt>**RPC \_ C \_ AuthN \_ dicembre \_ pubblico**</dt> <dt>4</dt> </dl>           | Autenticazione con chiave pubblica DEC. Riservato per utilizzi futuri.<br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <dt>**RPC \_ C \_ AuthN \_ GSS \_ Negotiate**</dt> <dt>9</dt> </dl>  | Security Support Provider Snego.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <dt>**RPC \_ \_ \_ WinNT auth**</dt> <dt>10</dt> di C </dl>                          | NTLMSSP<br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <dt>**RPC \_ C \_ AuthN \_ GSS \_ Schannel**</dt> <dt>14</dt> </dl>    | Security Support Provider Schannel. Questo servizio di autenticazione supporta SSL 2,0, SSL 3,0, TLS e PCT.<br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <dt>**RPC \_ Autenticazione del linguaggio C ( \_ \_ \_ Kerberos**</dt> ) a <dt>16</dt> </dl>    | Security Support Provider Kerberos.<br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <dt>**RPC \_ \_Autenticazione \_ DPA**</dt> <dt></dt> </dl>                                | Security Support Provider DPA.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <dt>**RPC \_ \_MSN AuthN \_ MSN**</dt> <dt>18</dt> </dl>                                | Security Support Provider MSN.<br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <dt>**RPC \_ \_ \_ Kernel AuthN C**</dt> <dt>20</dt> </dl>                       | Security Support Provider kernel.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <dt>**RPC \_ \_ \_ Digest di autenticazione C**</dt> <dt>21</dt> </dl>                       | Security Support Provider digest.<br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <dt>**RPC \_ \_ \_ Nego \_ Extender**</dt> <dt>30</dt> di autenticazione C </dl> | Security Support Provider Extender NEGO.<br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <dt>**RPC \_ C \_ auth \_ PKU2U**</dt> <dt>31</dt> </dl>                          | Security Support Provider PKU2U.<br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <dt>**RPC \_ C \_ AuthN \_ mq**</dt> <dt>100</dt> </dl>                                  | MQ Security Support Provider.<br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <dt>**RPC \_ 0xFFFFFFFF \_ \_ predefinito di autenticazione C**</dt> <dt></dt> </dl>           | Servizio di autenticazione predefinito del sistema. Quando si specifica questo valore, COM utilizza il normale algoritmo di negoziazione della copertura di sicurezza per selezionare un servizio di autenticazione. Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md). <br/> |



## <a name="remarks"></a>Commenti

Queste costanti vengono usate nel [**\_ \_ servizio di autenticazione esclusivo**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) e nelle uniche strutture di [**\_ \_ informazioni di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) . La struttura del **\_ \_ servizio di autenticazione unica** viene passata dal server alla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e può essere recuperata dalla funzione [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Un puntatore a una struttura di **\_ \_ informazioni di autenticazione unica** viene passato dal client a **CoInitializeSecurity**. Per ulteriori informazioni sui pacchetti di sicurezza identificati da questi valori, ad esempio NTLMSSP e Kerberos, vedere [pacchetti com e di sicurezza](com-and-security-packages.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[**\_informazioni di autenticazione esclusiva \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[**\_servizio di autenticazione esclusivo \_**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

