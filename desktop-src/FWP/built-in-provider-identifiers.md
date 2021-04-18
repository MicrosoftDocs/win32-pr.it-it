---
title: Identificatori provider predefiniti (Fwpmu. h)
description: Gli identificatori per i provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302196"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="245dc-103">Identificatori provider predefiniti</span><span class="sxs-lookup"><span data-stu-id="245dc-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="245dc-104">Gli identificatori per i provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID.</span><span class="sxs-lookup"><span data-stu-id="245dc-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="245dc-105">Questi identificatori sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="245dc-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="245dc-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_provider FWPM \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="245dc-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245dc-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="245dc-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="245dc-108">Usato per identificare tutti i filtri aggiunti da IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="245dc-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="245dc-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ \_ configurazione DOS IPSec provider \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="245dc-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245dc-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="245dc-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="245dc-111">Utilizzato per identificare tutti i filtri aggiunti dalla protezione DoS IPsec.</span><span class="sxs-lookup"><span data-stu-id="245dc-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="245dc-112">Disponibile solo in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="245dc-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="245dc-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_provider FWPM \_ TCP \_ Chimney \_ OFFLOAD**</span><span class="sxs-lookup"><span data-stu-id="245dc-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245dc-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span><span class="sxs-lookup"><span data-stu-id="245dc-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="245dc-115">Utilizzato per identificare tutti i filtri aggiunti da TCP Chimney Offload.</span><span class="sxs-lookup"><span data-stu-id="245dc-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="245dc-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ modelli TCP del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="245dc-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245dc-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="245dc-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="245dc-118">Utilizzato per identificare tutti i filtri aggiunti dai modelli TCP.</span><span class="sxs-lookup"><span data-stu-id="245dc-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="245dc-119">Disponibile solo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="245dc-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="245dc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="245dc-120">Requirements</span></span>



| <span data-ttu-id="245dc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="245dc-121">Requirement</span></span> | <span data-ttu-id="245dc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="245dc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="245dc-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="245dc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="245dc-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="245dc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="245dc-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="245dc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="245dc-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="245dc-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="245dc-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="245dc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="245dc-128"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="245dc-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





