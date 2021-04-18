---
description: I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Flag di riconnessione dinamica (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326927"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="b282d-103">Flag di riconnessione dinamica</span><span class="sxs-lookup"><span data-stu-id="b282d-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="b282d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b282d-104">\[Deprecated.</span></span> <span data-ttu-id="b282d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b282d-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="b282d-106">I flag seguenti specificano il livello di riconnessione dinamica da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="b282d-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="b282d-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b282d-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="b282d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b282d-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="b282d-109"><dt>**CONNECTF \_ \_Nessuno dinamico**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="b282d-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="b282d-110">Nessuna riconnessione dinamica.</span><span class="sxs-lookup"><span data-stu-id="b282d-110">No dynamic reconnection.</span></span> <span data-ttu-id="b282d-111">Caricare tutti gli elementi prima di eseguire il rendering del progetto.</span><span class="sxs-lookup"><span data-stu-id="b282d-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="b282d-112"><dt>**CONNECTF \_ \_Origini dinamiche**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="b282d-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="b282d-113">Caricare le origini solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="b282d-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="b282d-114"><dt>**CONNECTF \_ \_Effetti dinamici**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="b282d-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="b282d-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b282d-115">Reserved.</span></span> <span data-ttu-id="b282d-116">Non usare.</span><span class="sxs-lookup"><span data-stu-id="b282d-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="b282d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b282d-117">Requirements</span></span>



| <span data-ttu-id="b282d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b282d-118">Requirement</span></span> | <span data-ttu-id="b282d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b282d-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b282d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b282d-120">Header</span></span><br/> | <dl> <span data-ttu-id="b282d-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b282d-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b282d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b282d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b282d-123">**IRenderEngine::SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="b282d-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




