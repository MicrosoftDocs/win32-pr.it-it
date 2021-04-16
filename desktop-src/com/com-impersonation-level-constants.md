---
title: Costanti del livello di rappresentazione (RpcDce. h)
description: Specifica un livello di rappresentazione che indica la quantità di autorità assegnata al server durante la rappresentazione del client.
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
ms.openlocfilehash: c9f16ed07235e52d9aefd7bffff9ce430c3978d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340762"
---
# <a name="impersonation-level-constants"></a>Costanti del livello di rappresentazione

Specifica un livello di rappresentazione che indica la quantità di autorità assegnata al server durante la rappresentazione del client.



| Costante/valore                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ \_Livello Imp \_ \_ valore predefinito**</dt> <dt>0</dt> </dl>             | DCOM può scegliere il livello di rappresentazione utilizzando il normale algoritmo di negoziazione della copertura di sicurezza. Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ \_Livello Imp \_ \_ Anonimo**</dt> <dt>1</dt> </dl>       | Il client è anonimo per il server. Il processo server può rappresentare il client, ma il token di rappresentazione non conterrà alcuna informazione e non potrà essere utilizzato.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ Livello di C \_ Imp \_ \_ identificare**</dt> <dt>2</dt> </dl>          | Il server può ottenere l'identità del client. Il server può rappresentare il client per il controllo ACL, ma non può accedere agli oggetti di sistema come client. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ \_Rappresentazione a \_ livello \_ di C IMP**</dt> <dt>3</dt> </dl> | Il processo server può rappresentare il contesto di sicurezza del client quando agisce per conto del client. Questo livello di rappresentazione può essere usato per accedere a risorse locali, come ad esempio i file. Quando si rappresenta a questo livello, il token di rappresentazione può essere passato solo attraverso un limite di computer. Il servizio di autenticazione [Schannel](schannel.md) supporta solo questo livello di rappresentazione. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ \_Delegato a \_ livello \_ di C IMP**</dt> <dt>4</dt> </dl>          | Il processo server può rappresentare il contesto di sicurezza del client quando agisce per conto del client. Il processo server può inoltre effettuare chiamate in uscita ad altri server quando agisce per conto del client, utilizzando il mascheramento. Il server può usare il contesto di sicurezza del client in altri computer per accedere alle risorse locali e remote come client. Quando si rappresenta a questo livello, il token di rappresentazione può essere passato attraverso un numero qualsiasi di limiti del computer.<br/> |



## <a name="remarks"></a>Commenti

[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea) avrà esito negativo durante la rappresentazione a livello di identificazione. La soluzione alternativa consiste nel rappresentare, chiamare [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken), ripristinare, chiamare [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)e infine chiamare [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Utilizzando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), il client imposta il livello di rappresentazione

Utilizzando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), il client imposta il livello di rappresentazione e l'identità del proxy che saranno disponibili quando un server chiama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). L'identità che il server visualizzerà quando si esegue la rappresentazione è descritta in [mascheramento](cloaking.md). Si noti che quando si effettua una chiamata durante la rappresentazione, il chiamato riceve normalmente il token di processo del chiamante, non il token di rappresentazione del chiamante. Per ricevere il token di rappresentazione del chiamante, il chiamante deve abilitare il mascheramento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

