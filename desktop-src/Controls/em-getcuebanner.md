---
title: Messaggio EM_GETCUEBANNER (COMmctrl. h)
description: Ottiene il testo visualizzato come cue testuale, o suggerimento, in un controllo di modifica.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Controlli di Windows Message EM_GETCUEBANNER
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964899"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="de31a-104">\_Messaggio GETCUEBANNER em</span><span class="sxs-lookup"><span data-stu-id="de31a-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="de31a-105">Ottiene il testo visualizzato come cue testuale, o suggerimento, in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="de31a-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="de31a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de31a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de31a-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de31a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de31a-108">Puntatore a un buffer Unicode che riceve il testo impostato come cue testuale.</span><span class="sxs-lookup"><span data-stu-id="de31a-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="de31a-109">Il chiamante è responsabile dell'allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="de31a-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="de31a-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de31a-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de31a-111">Dimensione del buffer a cui punta *wParam* in **WCHAR**, inclusa la terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="de31a-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de31a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de31a-112">Return value</span></span>

<span data-ttu-id="de31a-113">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="de31a-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="de31a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="de31a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="de31a-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="de31a-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="de31a-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de31a-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de31a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de31a-117">Requirements</span></span>



| <span data-ttu-id="de31a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de31a-118">Requirement</span></span> | <span data-ttu-id="de31a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="de31a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de31a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de31a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de31a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de31a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de31a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de31a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de31a-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de31a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de31a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de31a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de31a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de31a-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de31a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de31a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de31a-127">**Modifica \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="de31a-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





