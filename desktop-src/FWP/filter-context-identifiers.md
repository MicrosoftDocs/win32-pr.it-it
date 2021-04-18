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
# <a name="filter-context-identifiers"></a><span data-ttu-id="437cd-103">Identificatori di contesto di filtro</span><span class="sxs-lookup"><span data-stu-id="437cd-103">Filter Context Identifiers</span></span>

<span data-ttu-id="437cd-104">Gli identificatori per i contesti di filtro incorporati nella piattaforma filtro Windows sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="437cd-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="437cd-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**contesto FWPM in \_ \_ ingresso IPSec in ingresso \_ \_ , FWPM \_ contesto IPSec in \_ \_ ingresso \_ Mantieni \_ \_ sicurezza connessione, FWPM \_ contesto IPSec in \_ \_ ingresso \_ riservato**</span><span class="sxs-lookup"><span data-stu-id="437cd-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-106">Contesti di filtro del trasporto IPsec nel livello in ingresso.</span><span class="sxs-lookup"><span data-stu-id="437cd-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="437cd-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM \_ contesto \_ IPSec in \_ uscita \_ Negotiate \_ di negoziazione, FWPM \_ contesto \_ IPSec in \_ uscita \_ \_**</span><span class="sxs-lookup"><span data-stu-id="437cd-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-108">Contesti di filtro del trasporto IPsec nel livello in uscita.</span><span class="sxs-lookup"><span data-stu-id="437cd-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="437cd-109">Per Windows 7, utilizzare **la \_ \_ negoziazione in \_ uscita IPSec \_ in \_ uscita del contesto FWPM**.</span><span class="sxs-lookup"><span data-stu-id="437cd-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="437cd-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ contesto \_ ale \_ set \_ Connection \_ richiede \_ la \_ sicurezza IPSec, FWPM \_ Context \_ ale \_ set \_ Connection \_ Lazy \_ SD \_ Evaluation**</span><span class="sxs-lookup"><span data-stu-id="437cd-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-111">Contesti di filtro usati nel livello ALE Connect.</span><span class="sxs-lookup"><span data-stu-id="437cd-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="437cd-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ contesto \_ ale \_ set \_ Connection \_ richiede \_ la \_ crittografia IPSec, FWPM \_ Context \_ ale \_ set \_ Connection \_ Consenti First in \_ \_ ingresso \_ PKT \_ decrittografato, FWPM \_ Context \_ ale \_ Consenti \_ autorizzazione \_ FW**</span><span class="sxs-lookup"><span data-stu-id="437cd-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-113">Contesti di filtro usati nel livello di ALE Connect o Accept.</span><span class="sxs-lookup"><span data-stu-id="437cd-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="437cd-114">Per Windows 7, usare **FWPM \_ Context \_ ale \_ set \_ Connection \_ Consenti \_ First in \_ ingresso \_ PKT \_ unencrypted** o **FWPM \_ Context \_ ale \_ allow \_ auth \_ FW**.</span><span class="sxs-lookup"><span data-stu-id="437cd-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="437cd-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_contesto FWPM \_ TCP \_ Chimney \_ offload \_ abilitata, \_ contesto FWPM \_ TCP \_ Chimney \_ offload \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="437cd-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-116">Contesti utilizzati dai callout del TCP Chimney Offload.</span><span class="sxs-lookup"><span data-stu-id="437cd-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="437cd-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_controllo RPC del contesto FWPM \_ \_ \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="437cd-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="437cd-118">Contesti utilizzati nel sottolivello di controllo RPC.</span><span class="sxs-lookup"><span data-stu-id="437cd-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="437cd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="437cd-119">Requirements</span></span>



| <span data-ttu-id="437cd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="437cd-120">Requirement</span></span> | <span data-ttu-id="437cd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="437cd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="437cd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="437cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="437cd-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="437cd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="437cd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="437cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="437cd-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="437cd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="437cd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="437cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="437cd-127"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="437cd-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





