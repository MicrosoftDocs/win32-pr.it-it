---
title: Messaggio EM_HIDEBALLOONTIP (COMmctrl. h)
description: Nasconde qualsiasi suggerimento del fumetto associato a un controllo di modifica.
ms.assetid: 820b98d6-c2bd-4821-ba44-9d58e23eac81
keywords:
- Controlli di Windows Message EM_HIDEBALLOONTIP
topic_type:
- apiref
api_name:
- EM_HIDEBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ecececff3d12ad48cfcfb6353a717e8f8875df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963833"
---
# <a name="em_hideballoontip-message"></a><span data-ttu-id="cfdbd-104">\_Messaggio HIDEBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="cfdbd-104">EM\_HIDEBALLOONTIP message</span></span>

<span data-ttu-id="cfdbd-105">Nasconde qualsiasi suggerimento del fumetto associato a un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-105">Hides any balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfdbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfdbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfdbd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfdbd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfdbd-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cfdbd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfdbd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfdbd-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfdbd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfdbd-111">Return value</span></span>

<span data-ttu-id="cfdbd-112">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="cfdbd-113">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfdbd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfdbd-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfdbd-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="cfdbd-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cfdbd-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfdbd-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfdbd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfdbd-117">Requirements</span></span>



| <span data-ttu-id="cfdbd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfdbd-118">Requirement</span></span> | <span data-ttu-id="cfdbd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cfdbd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfdbd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfdbd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdbd-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfdbd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfdbd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfdbd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdbd-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfdbd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfdbd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfdbd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfdbd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfdbd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfdbd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfdbd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdbd-127">**Modifica \_ HideBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="cfdbd-127">**Edit\_HideBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_hideballoontip)
</dt> </dl>

 

 





