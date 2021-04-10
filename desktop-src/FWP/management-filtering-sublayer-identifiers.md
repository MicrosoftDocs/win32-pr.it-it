---
title: Filtraggio degli identificatori di sottolivello (Fwpmu. h)
description: Gestione API PAM filtro delle costanti dell'identificatore di sottolivello.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874301"
---
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="832f2-103">Filtraggio degli identificatori di sottolivello</span><span class="sxs-lookup"><span data-stu-id="832f2-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="832f2-104">Gli identificatori del sottolivello Windows Filtering Platform (WFP) sono rappresentati da un GUID.</span><span class="sxs-lookup"><span data-stu-id="832f2-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="832f2-105">Questi identificatori sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="832f2-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="832f2-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM sublayer \_ \_ Edge \_ Traversal/FWPM \_ sottolivello \_ TEREDO**</span><span class="sxs-lookup"><span data-stu-id="832f2-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-107">I filtri di attraversamento bordi vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="832f2-108">Per Windows 7 e versioni successive, usare l' **\_ \_ \_ attraversamento dei confini del sottolivello FWPM**.</span><span class="sxs-lookup"><span data-stu-id="832f2-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_ispezione del SOTTOLIVELLO FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-110">Si tratta del sottolivello ponderato più basso.</span><span class="sxs-lookup"><span data-stu-id="832f2-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="832f2-111">Viene usato solo per i filtri di ispezione.</span><span class="sxs-lookup"><span data-stu-id="832f2-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_DoSP IPSec FWPM SUBlayer \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-113">I filtri di protezione DoS IPsec vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="832f2-114">Disponibile solo in Windows Vista con SP1, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="832f2-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ tunnel in uscita da IPSec in \_ uscita \_ del sottolivello FWPM**</span><span class="sxs-lookup"><span data-stu-id="832f2-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-116">I filtri di tunneling in uscita IPsec vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="832f2-117">Disponibile solo in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="832f2-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_tunnel IPSec del SOTTOLIVELLO FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-119">I filtri del tunnel IPsec vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_labbri sottostrato FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-121">I filtri IPsec legacy vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_controllo RPC SOTTOLIVELLO FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-123">I filtri di controllo RPC vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="832f2-124">Questi filtri controllano le chiamate in ingresso RPC come parte di C2 e la conformità ai criteri comuni.</span><span class="sxs-lookup"><span data-stu-id="832f2-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_socket sicuro del SOTTOLIVELLO FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-126">I filtri socket protetti vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ TCP \_ Chimney \_ OFFLOAD di FWPM sublayer**</span><span class="sxs-lookup"><span data-stu-id="832f2-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-128">I filtri TCP Chimney Offload vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_modelli TCP del SOTTOLIVELLO FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="832f2-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-130">I filtri dei modelli TCP vengono aggiunti a questo sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="832f2-131">Disponibile solo in Windows 8, Windows Server 2012 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="832f2-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="832f2-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ sublayer \_ universale**</span><span class="sxs-lookup"><span data-stu-id="832f2-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="832f2-133">Questo sottolivello ospita tutti i filtri che non sono assegnati ad alcun altro sottolivello.</span><span class="sxs-lookup"><span data-stu-id="832f2-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="832f2-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="832f2-134">Requirements</span></span>



| <span data-ttu-id="832f2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="832f2-135">Requirement</span></span> | <span data-ttu-id="832f2-136">Valore</span><span class="sxs-lookup"><span data-stu-id="832f2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="832f2-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="832f2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="832f2-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="832f2-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="832f2-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="832f2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="832f2-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="832f2-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="832f2-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="832f2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="832f2-142"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="832f2-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





