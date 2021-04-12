---
title: Sfocature di DWM dietro costanti (dwmapi. h)
description: Flag utilizzati dalla \_ struttura BLURBEHIND di DWM per indicare quali membri contengono informazioni valide.
ms.assetid: d6dd552c-1f3b-4f16-8705-f5016ed55d9e
topic_type:
- apiref
api_name:
- DWM_BB_ENABLE
- DWM_BB_BLURREGION
- DWM_BB_TRANSITIONONMAXIMIZED
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe08e0315d4c4b906cdb897ac7ad5dd34d50fbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518130"
---
# <a name="dwm-blur-behind-constants"></a><span data-ttu-id="3eea9-103">Sfocature di DWM dietro costanti</span><span class="sxs-lookup"><span data-stu-id="3eea9-103">DWM Blur Behind Constants</span></span>

<span data-ttu-id="3eea9-104">Flag utilizzati dalla struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) per indicare quali membri contengono informazioni valide.</span><span class="sxs-lookup"><span data-stu-id="3eea9-104">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span>

<dl> <dt>

<span data-ttu-id="3eea9-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**\_Abilitazione di DWM BB \_**</span><span class="sxs-lookup"><span data-stu-id="3eea9-105"><span id="DWM_BB_ENABLE"></span><span id="dwm_bb_enable"></span>**DWM\_BB\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eea9-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3eea9-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="3eea9-107">È stato specificato un valore per il membro **fEnable** .</span><span class="sxs-lookup"><span data-stu-id="3eea9-107">A value for the **fEnable** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3eea9-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**\_BLURREGION BB \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="3eea9-108"><span id="DWM_BB_BLURREGION"></span><span id="dwm_bb_blurregion"></span>**DWM\_BB\_BLURREGION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eea9-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3eea9-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="3eea9-110">È stato specificato un valore per il membro **hRgnBlur** .</span><span class="sxs-lookup"><span data-stu-id="3eea9-110">A value for the **hRgnBlur** member has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3eea9-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**\_TRANSITIONONMAXIMIZED BB \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="3eea9-111"><span id="DWM_BB_TRANSITIONONMAXIMIZED"></span><span id="dwm_bb_transitiononmaximized"></span>**DWM\_BB\_TRANSITIONONMAXIMIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eea9-112">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3eea9-112">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="3eea9-113">È stato specificato un valore per il membro **fTransitionOnMaximized** .</span><span class="sxs-lookup"><span data-stu-id="3eea9-113">A value for the **fTransitionOnMaximized** member has been specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3eea9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eea9-114">Requirements</span></span>



| <span data-ttu-id="3eea9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eea9-115">Requirement</span></span> | <span data-ttu-id="3eea9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3eea9-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3eea9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eea9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3eea9-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3eea9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3eea9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eea9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3eea9-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3eea9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3eea9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3eea9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eea9-122"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eea9-122"><dt>Dwmapi.h</dt></span></span> </dl> |



 

 





