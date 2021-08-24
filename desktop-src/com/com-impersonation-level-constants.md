---
title: Costanti del livello di rappresentazione (RpcDce.h)
description: Specifica un livello di rappresentazione, che indica la quantità di autorità data al server quando rappresenta il client.
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048489"
---
# <a name="impersonation-level-constants"></a>Costanti del livello di rappresentazione

Specifica un livello di rappresentazione, che indica la quantità di autorità data al server quando rappresenta il client.



| Costante/valore                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ LIVELLO \_ IMP \_ C \_ PREDEFINITO**</dt> <dt>0</dt> </dl>             | DCOM può scegliere il livello di rappresentazione usando il normale algoritmo di negoziazione della protezione generale. Per altre informazioni, vedere [Negoziazione con copertura della sicurezza](security-blanket-negotiation.md).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS**</dt> <dt>1</dt> </dl>       | Il client è anonimo per il server. Il processo server può rappresentare il client, ma il token di rappresentazione non conterrà informazioni e non potrà essere usato.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY**</dt> <dt>2</dt> </dl>          | Il server può ottenere l'identità del client. Il server può rappresentare il client per il controllo ACL, ma non può accedere agli oggetti di sistema come client. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE**</dt> <dt>3</dt> </dl> | Il processo server può rappresentare il contesto di sicurezza del client agendo per conto del client. Questo livello di rappresentazione può essere usato per accedere a risorse locali, come ad esempio i file. Quando si esegue la rappresentazione a questo livello, il token di rappresentazione può essere passato solo attraverso un limite del computer. Il [servizio di autenticazione Schannel](schannel.md) supporta solo questo livello di rappresentazione. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ DELEGATO \_ DI \_ LIVELLO \_ IMP C**</dt> <dt>4</dt> </dl>          | Il processo server può rappresentare il contesto di sicurezza del client agendo per conto del client. Il processo server può anche effettuare chiamate in uscita ad altri server mentre agisce per conto del client, usando la clonazione. Il server può usare il contesto di sicurezza del client in altri computer per accedere alle risorse locali e remote come client. Quando si esegue la rappresentazione a questo livello, il token di rappresentazione può essere passato attraverso qualsiasi numero di limiti del computer.<br/> |



## <a name="remarks"></a>Commenti

[**GetUserName avrà esito**](/windows/desktop/api/winbase/nf-winbase-getusernamea) negativo durante la rappresentazione a livello di identificazione. La soluzione alternativa consiste nel rappresentare, [**chiamare OpenThreadToken,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)ripristinare, [**chiamare GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)e infine [**chiamare LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Usando [**CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)il client imposta il livello di rappresentazione

Usando [**CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)il client imposta il livello di rappresentazione e l'identità proxy che saranno disponibili quando un server chiama [**CoImpersonateClient.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) L'identità che verrà visualizzata dal server durante la rappresentazione è descritta in [Cloaking](cloaking.md). Si noti che quando si effettua una chiamata durante la rappresentazione, il chiamato riceverà in genere il token di processo del chiamante, non il token di rappresentazione del chiamante. Per ricevere il token di rappresentazione del chiamante, il chiamante deve abilitare il cloaking.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>RpcDce.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

