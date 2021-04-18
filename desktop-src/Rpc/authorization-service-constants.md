---
title: Costanti Authorization-Service (rpcdce. h)
description: Le costanti del servizio di autorizzazione rappresentano i servizi di autorizzazione passati a varie funzioni di run-time.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519262"
---
# <a name="authorization-service-constants"></a>Costanti Authorization-Service

Le costanti del servizio di autorizzazione rappresentano i servizi di autorizzazione passati a varie funzioni di run-time.

Le costanti seguenti sono valori validi per il parametro *AuthzSvc* . La maggior parte delle applicazioni trova \_ AUTHZ RPC C \_ \_ non sufficienti.



| Costante/valore                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ None**</dt> <dt>0</dt> </dl>                   | Il server non esegue alcuna autorizzazione.<br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ nome**</dt> <dt>1</dt> </dl>                   | Il server esegue l'autorizzazione in base al nome principale del client.<br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ DCE**</dt> <dt>2</dt> </dl>                      | Il server esegue il controllo delle autorizzazioni utilizzando le informazioni del certificato dell'attributo Privilege (PAC) del client, che viene inviato al server con ogni chiamata di procedura remota eseguita utilizzando l'handle di associazione. In genere, l'accesso viene controllato rispetto agli elenchi di controllo di accesso ([ACL](/windows/desktop/api/winnt/ns-winnt-acl)) DCE.<br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <dt>**RPC \_ C \_ AUTHZ \_ predefinito**</dt> <dt>0xFFFFFFFF</dt> </dl> | Il server utilizza il servizio di autorizzazione predefinito per il provider di servizi condivisi corrente.<br/>                                                                                                                                                                                                                                |



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
</dt> <dt>

[**RpcMgmtInqDefaultProtectLevel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

