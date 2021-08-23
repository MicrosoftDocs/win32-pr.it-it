---
title: Costanti di autorizzazione (RpcDce.h)
description: Definisce ciò che il server autorizza.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb89786a0c27c66177bc29861fdcf53a9341f73e498b5627e1cb826e83f61cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048669"
---
# <a name="authorization-constants"></a>Costanti di autorizzazione

Definisce ciò che il server autorizza.



| Costante/valore                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NONE**</dt> <dt>0</dt> </dl>                   | Il server non esegue alcuna autorizzazione. Attualmente, RPC \_ C \_ AUTHN \_ WINNT, RPC \_ C \_ AUTHN \_ GSS \_ SCHANNEL e RPC C \_ AUTHN GSS KERBEROS usano solo RPC C \_ \_ \_ \_ \_ AUTHZ \_ NONE.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ NAME**</dt> <dt>1</dt> </dl>                   | Il server esegue l'autorizzazione in base al nome dell'entità del client. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Il server esegue il controllo delle autorizzazioni usando le informazioni del certificato dell'attributo privilegio (PAC) DCE del client, che vengono inviate al server con ogni chiamata di procedura remota effettuata usando l'handle di associazione. In genere, l'accesso viene controllato in base agli elenchi di controllo di accesso (ACL) DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DEFAULT**</dt> <dt>0xffffffff</dt> </dl> | DCOM può scegliere il livello di autorizzazione usando il normale algoritmo di negoziazione di negoziazione di sicurezza. Per altre informazioni, vedere [Negoziazione di negoziazione della negoziazione della sicurezza.](security-blanket-negotiation.md)<br/>                                                                                           |



## <a name="remarks"></a>Commenti

Queste costanti vengono usate dai metodi [**dell'interfaccia IClientSecurity.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Vengono usati nella struttura [**SOLE \_ AUTHENTICATION \_ SERVICE,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) recuperata dalla [**funzione CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) Vengono inoltre usati nella struttura [**SOLE \_ AUTHENTICATION \_ INFO,**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) che a sua volta è un membro della [**struttura SOLE AUTHENTICATION \_ \_ LIST.**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) Questa struttura, ovvero un elenco di servizi di autenticazione, i servizi di autorizzazione che eseguono e le informazioni di autenticazione per ogni servizio, viene passata alla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e al metodo [**IClientSecurity::SetBlanket.**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)

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

 

