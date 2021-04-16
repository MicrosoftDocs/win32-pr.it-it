---
title: Costanti del livello di autenticazione (rpcdce. h)
description: Questi valori specificano un livello di autenticazione che indica la quantità di autenticazione fornita per aiutare a proteggere l'integrità dei dati. Ogni livello include la protezione fornita dai livelli precedenti.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
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
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519062"
---
# <a name="authentication-level-constants"></a>Costanti del livello di autenticazione

Questi valori specificano un livello di autenticazione che indica la quantità di autenticazione fornita per aiutare a proteggere l'integrità dei dati. Ogni livello include la protezione fornita dai livelli precedenti.



| Costante/valore                                                                                                                                                                                                                                                                 | Descrizione                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <dt>**RPC \_ \_ \_ Livello \_ predefinito di autenticazione C**</dt> <dt>0</dt> </dl>                    | Indica a DCOM di scegliere il livello di autenticazione utilizzando il normale algoritmo di negoziazione della copertura di sicurezza. Per ulteriori informazioni, vedere la pagina relativa alla [negoziazione della copertura di sicurezza](security-blanket-negotiation.md). <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <dt>**RPC \_ \_Livello autenticazione C \_ \_ None**</dt> <dt>1</dt> </dl>                             | Non esegue alcuna autenticazione.<br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <dt>**RPC \_ \_Livello di autenticazione \_ C \_ Connect**</dt> <dt>2</dt> </dl>                    | Autentica le credenziali del client solo quando il client stabilisce una relazione con il server. I trasporti di datagramma utilizzano sempre \_ PKT a livello di autenticazione RPC \_ \_ . <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <dt>**RPC \_ \_ \_ \_ Chiamata a livello di autenticazione C**</dt> <dt>3</dt> </dl>                             | Esegue l'autenticazione solo all'inizio di ogni chiamata di procedura remota quando il server riceve la richiesta. I trasporti di datagramma usano \_ \_ invece PKT a livello auth C RPC \_ \_ .<br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT**</dt> <dt>4</dt> </dl>                                | Autentica che tutti i dati ricevuti provengano dal client previsto.<br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT \_ integrità**</dt> <dt>5</dt> </dl> | Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.<br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <dt>**RPC \_ \_Livello di autenticazione \_ C \_ PKT \_ privacy**</dt> <dt>6</dt> </dl>       | Autentica tutti i livelli precedenti e crittografa il valore dell'argomento di ogni chiamata di procedura remota.<br/>                                                                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





