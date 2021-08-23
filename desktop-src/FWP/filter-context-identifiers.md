---
title: Identificatori di contesto di filtro (Fwpmu.h)
description: Identificatori per i contesti di filtro incorporati in Windows Filtering Platform.
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
ms.openlocfilehash: fdc7d9914a9b6089ace87e7e9b942499d8e65dc7705bf524f74cddf96ee419d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951270"
---
# <a name="filter-context-identifiers"></a>Filtrare gli identificatori di contesto

Gli identificatori per i contesti di filtro incorporati nella Windows di filtro sono definiti come segue.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PASSTHRU, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY, FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ RESERVED**
</dt> <dd> <dl> <dt>



Contesti di filtro del trasporto IPsec nel livello in ingresso.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**INDIVIDUAZIONE NEGOZIAZIONE IN USCITA IPSEC CONTESTO FWPM, INDIVIDUAZIONE DELLA NEGOZIAZIONE IN USCITA DEL CONTESTO \_ \_ \_ \_ \_ FWPM \_ \_ IPSEC \_ ELIMINAZIONE \_ \_ NEGOZIAZIONE IN USCITA**
</dt> <dd> <dl> <dt>



Contesti di filtro del trasporto IPsec nel livello in uscita.

> [!Note]  
> Per Windows 7, usare **FWPM \_ CONTEXT \_ IPSEC OUTBOUND SUPPRESS \_ \_ \_ NEGOTIATION**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ SECURITY, FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ LAZY \_ SD \_ EVALUATION**
</dt> <dd> <dl> <dt>



Filtrare i contesti usati nel livello di connessione ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ REQUIRE \_ IPSEC \_ ENCRYPTION, FWPM \_ CONTEXT \_ ALE \_ SET \_ CONNECTION \_ ALLOW \_ FIRST \_ INBOUND \_ PKT \_ UNENCRYPTED, FWPM \_ CONTEXT \_ ALE \_ ALLOW \_ AUTH \_ FW**
</dt> <dd> <dl> <dt>



Filtrare i contesti usati nel livello ale connect o accept.

> [!Note]  
> Per Windows 7, usare **FWPM \_ CONTEXT \_ ALE \_ SET CONNECTION ALLOW \_ FIRST \_ \_ \_ INBOUND \_ PKT \_ UNENCRYPTED** o **FWPM \_ CONTEXT \_ ALE ALLOW \_ \_ AUTH \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ ENABLE, FWPM \_ CONTEXT \_ TCP \_ CHIMNEY \_ OFFLOAD \_ DISABLE**
</dt> <dd> <dl> <dt>



Contesti usati dai TCP Chimney Offload callout.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**CONTROLLO RPC DEL CONTESTO FWPM \_ \_ \_ \_ ABILITATO**
</dt> <dd> <dl> <dt>



Contesti usati nel sottolivente di controllo RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





