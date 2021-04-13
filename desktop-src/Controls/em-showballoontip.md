---
title: Messaggio EM_SHOWBALLOONTIP (COMmctrl. h)
description: Il \_ messaggio SHOWBALLOONTIP em Visualizza un fumetto suggerimento associato a un controllo di modifica.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Controlli di Windows Message EM_SHOWBALLOONTIP
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120122"
---
# <a name="em_showballoontip-message"></a><span data-ttu-id="54c9d-104">\_Messaggio SHOWBALLOONTIP em</span><span class="sxs-lookup"><span data-stu-id="54c9d-104">EM\_SHOWBALLOONTIP message</span></span>

<span data-ttu-id="54c9d-105">Il **messaggio \_ SHOWBALLOONTIP em** Visualizza un fumetto suggerimento associato a un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54c9d-105">The **EM\_SHOWBALLOONTIP** message displays a balloon tip associated with an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="54c9d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54c9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54c9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54c9d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54c9d-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="54c9d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="54c9d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54c9d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54c9d-110">Puntatore a una struttura [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) che contiene informazioni sul fumetto suggerimento da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="54c9d-110">A pointer to an [**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) structure that contains information about the balloon tip to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54c9d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54c9d-111">Return value</span></span>

<span data-ttu-id="54c9d-112">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="54c9d-112">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="54c9d-113">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="54c9d-113">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c9d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="54c9d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54c9d-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="54c9d-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="54c9d-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="54c9d-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54c9d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54c9d-117">Requirements</span></span>



| <span data-ttu-id="54c9d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54c9d-118">Requirement</span></span> | <span data-ttu-id="54c9d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="54c9d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54c9d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54c9d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54c9d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54c9d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54c9d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54c9d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54c9d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54c9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c9d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54c9d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c9d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54c9d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="54c9d-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="54c9d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54c9d-128">**EDITBALLOONTIP**</span><span class="sxs-lookup"><span data-stu-id="54c9d-128">**EDITBALLOONTIP**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[<span data-ttu-id="54c9d-129">**Modifica \_ ShowBalloonTip**</span><span class="sxs-lookup"><span data-stu-id="54c9d-129">**Edit\_ShowBalloonTip**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





