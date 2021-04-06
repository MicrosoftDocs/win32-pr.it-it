---
title: Costanti di autorizzazione (RpcDce. h)
description: Definisce gli elementi autorizzati dal server.
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
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743711"
---
# <a name="authorization-constants"></a>Costanti di autorizzazione

Definisce gli elementi autorizzati dal server.



| Costante/valore                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | Il server non esegue alcuna autorizzazione. Attualmente, le autorizzazioni RPC c AuthN \_ \_ \_ WinNT, RPC \_ c \_ AuthN \_ GSS \_ Schannel e RPC \_ c \_ AuthN \_ GSS \_ Kerberos utilizzano solo RPC \_ c \_ AUTHZ \_ None.<br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt> </dl>                   | Il server esegue l'autorizzazione in base al nome principale del client. <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Il server esegue il controllo delle autorizzazioni utilizzando le informazioni del certificato dell'attributo Privilege (PAC) del client, che viene inviato al server con ogni chiamata di procedura remota eseguita utilizzando l'handle di associazione. In genere, l'accesso viene controllato rispetto agli elenchi di controllo di accesso (ACL) DCE. <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ predefinito**</dt> <dt>0xFFFFFFFF</dt> </dl> | DCOM può scegliere il livello di autorizzazione utilizzando il normale algoritmo di negoziazione della copertura di sicurezza. Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md).<br/>                                                                                           |



## <a name="remarks"></a>Commenti

Queste costanti vengono usate dai metodi dell'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Vengono usati nell'unica struttura [**del \_ \_ servizio di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) , che viene recuperata dalla funzione [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) . Vengono inoltre usati nell'unica struttura [**di \_ \_ informazioni di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) , che a sua volta è un membro della struttura dell' [**unico \_ \_ elenco di autenticazione**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) . Questa struttura, ovvero un elenco di servizi di autenticazione, i servizi di autorizzazione che eseguono e le informazioni di autenticazione per ogni servizio, vengono passati alla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e al metodo [**IClientSecurity:: seblank**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) .

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

 

