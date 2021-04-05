---
title: CFSTR_DS_DISPLAY_SPEC_OPTIONS (DSClient. h)
description: Il formato degli Appunti per le opzioni di visualizzazione di CFSTR \_ DS \_ \_ \_ fornisce un HGLOBAL che contiene una struttura DSDISPLAYSPECOPTIONS.
ms.assetid: 98e033e4-14fe-44ed-83d5-a97e00ecce4c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DS_DISPLAY_SPEC_OPTIONS
- CFSTR_DSDISPLAYSPECOPTIONS
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81f3a229971be5ecfb9ec2c86e166af27f94e01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048209"
---
# <a name="cfstr_ds_display_spec_options"></a><span data-ttu-id="9c5c1-103">\_ \_ \_ Opzioni specifiche per la visualizzazione di CFSTR DS \_</span><span class="sxs-lookup"><span data-stu-id="9c5c1-103">CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS</span></span>

<dl> <dt>

<span data-ttu-id="9c5c1-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**\_ \_ \_ Opzioni specifiche per la visualizzazione di CFSTR DS \_**</span><span class="sxs-lookup"><span data-stu-id="9c5c1-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c5c1-105">"DsDisplaySpecOptions"</span><span class="sxs-lookup"><span data-stu-id="9c5c1-105">"DsDisplaySpecOptions"</span></span>
</dt> <dt>



<span data-ttu-id="9c5c1-106">Il Active Directory utenti e computer, i siti e i servizi Active Directory e gli snap-in domini e trust Active Directory supportano il formato degli Appunti per le opzioni per la **visualizzazione di CFSTR \_ DS \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="9c5c1-106">The Active Directory Users and Computers, the Active Directory Sites and Services, and the Active Directory Domains and Trusts snap-ins support the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span> <span data-ttu-id="9c5c1-107">Il formato degli Appunti per le **\_ \_ \_ \_ Opzioni di visualizzazione di CFSTR DS** fornisce un **HGLOBAL** che contiene una struttura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) .</span><span class="sxs-lookup"><span data-stu-id="9c5c1-107">The **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format provides an **HGLOBAL** that contains a [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) structure.</span></span> <span data-ttu-id="9c5c1-108">**DSDISPLAYSPECOPTIONS** contiene i dati di configurazione per l'utilizzo da parte dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="9c5c1-108">The **DSDISPLAYSPECOPTIONS** contains configuration data for use by the extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9c5c1-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**\_DSDISPLAYSPECOPTIONS CFSTR**</span><span class="sxs-lookup"><span data-stu-id="9c5c1-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR\_DSDISPLAYSPECOPTIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9c5c1-110">Il formato degli Appunti **\_ DSDISPLAYSPECOPTIONS di CFSTR** è identico al formato degli Appunti per le **\_ \_ \_ \_ Opzioni di visualizzazione di CFSTR DS** .</span><span class="sxs-lookup"><span data-stu-id="9c5c1-110">The **CFSTR\_DSDISPLAYSPECOPTIONS** clipboard format is identical to the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c5c1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c5c1-111">Requirements</span></span>



| <span data-ttu-id="9c5c1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c5c1-112">Requirement</span></span> | <span data-ttu-id="9c5c1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5c1-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5c1-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c5c1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9c5c1-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c5c1-115">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9c5c1-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c5c1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9c5c1-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c5c1-117">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9c5c1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c5c1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c5c1-119"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c5c1-119"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c5c1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c5c1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c5c1-121">**DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="9c5c1-121">**DSDISPLAYSPECOPTIONS**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)
</dt> </dl>

 

 





