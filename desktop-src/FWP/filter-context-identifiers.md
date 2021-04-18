---
title: Identificatori di contesto di filtro (Fwpmu. h)
description: Identificatori per i contesti di filtro incorporati nella piattaforma filtro Windows.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302355"
---
# <a name="filter-context-identifiers"></a>Identificatori di contesto di filtro

Gli identificatori per i contesti di filtro incorporati nella piattaforma filtro Windows sono definiti nel modo seguente.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**contesto FWPM in \_ \_ ingresso IPSec in ingresso \_ \_ , FWPM \_ contesto IPSec in \_ \_ ingresso \_ Mantieni \_ \_ sicurezza connessione, FWPM \_ contesto IPSec in \_ \_ ingresso \_ riservato**
</dt> <dd> <dl> <dt>



Contesti di filtro del trasporto IPsec nel livello in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ contesto \_ IPSec in \_ uscita \_ Negotiate \_ di negoziazione, FWPM \_ contesto \_ IPSec in \_ uscita \_ \_**
</dt> <dd> <dl> <dt>



Contesti di filtro del trasporto IPsec nel livello in uscita.

> [!Note]  
> Per Windows 7, utilizzare **la \_ \_ negoziazione in \_ uscita IPSec \_ in \_ uscita del contesto FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ contesto \_ ale \_ set \_ Connection \_ richiede \_ la \_ sicurezza IPSec, FWPM \_ Context \_ ale \_ set \_ Connection \_ Lazy \_ SD \_ Evaluation**
</dt> <dd> <dl> <dt>



Contesti di filtro usati nel livello ALE Connect.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ contesto \_ ale \_ set \_ Connection \_ richiede \_ la \_ crittografia IPSec, FWPM \_ Context \_ ale \_ set \_ Connection \_ Consenti First in \_ \_ ingresso \_ PKT \_ decrittografato, FWPM \_ Context \_ ale \_ Consenti \_ autorizzazione \_ FW**
</dt> <dd> <dl> <dt>



Contesti di filtro usati nel livello di ALE Connect o Accept.

> [!Note]  
> Per Windows 7, usare **FWPM \_ Context \_ ale \_ set \_ Connection \_ Consenti \_ First in \_ ingresso \_ PKT \_ unencrypted** o **FWPM \_ Context \_ ale \_ allow \_ auth \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_contesto FWPM \_ TCP \_ Chimney \_ offload \_ abilitata, \_ contesto FWPM \_ TCP \_ Chimney \_ offload \_ disabilitato**
</dt> <dd> <dl> <dt>



Contesti utilizzati dai callout del TCP Chimney Offload.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_controllo RPC del contesto FWPM \_ \_ \_ abilitato**
</dt> <dd> <dl> <dt>



Contesti utilizzati nel sottolivello di controllo RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





