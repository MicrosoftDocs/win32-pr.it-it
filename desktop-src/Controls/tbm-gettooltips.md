---
title: Messaggio TBM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip assegnato a TrackBar, se presente.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Controlli di Windows Message TBM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873829"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="32770-104">\_Messaggio TBM GETtooltips</span><span class="sxs-lookup"><span data-stu-id="32770-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="32770-105">Recupera l'handle per il controllo ToolTip assegnato a TrackBar, se presente.</span><span class="sxs-lookup"><span data-stu-id="32770-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="32770-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32770-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32770-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32770-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="32770-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32770-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32770-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32770-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="32770-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32770-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32770-111">Return value</span></span>

<span data-ttu-id="32770-112">Restituisce l'handle per il controllo ToolTip assegnato a TrackBar oppure **null** se le descrizioni comandi non sono in uso.</span><span class="sxs-lookup"><span data-stu-id="32770-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="32770-113">Se il controllo TrackBar non usa lo stile [**delle \_ descrizioni comandi di TBS**](trackbar-control-styles.md) , il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="32770-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="32770-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32770-114">Requirements</span></span>



| <span data-ttu-id="32770-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32770-115">Requirement</span></span> | <span data-ttu-id="32770-116">Valore</span><span class="sxs-lookup"><span data-stu-id="32770-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32770-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32770-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32770-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32770-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32770-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32770-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32770-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32770-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32770-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32770-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32770-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32770-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





