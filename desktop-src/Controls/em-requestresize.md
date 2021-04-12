---
title: Messaggio di EM_REQUESTRESIZE (RichEdit. h)
description: Impone a un controllo Rich Edit di inviare un \_ codice di notifica en REQUESTRESIZE alla finestra padre.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Controlli di Windows Message EM_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225237"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="e579d-104">\_Messaggio REQUESTRESIZE em</span><span class="sxs-lookup"><span data-stu-id="e579d-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="e579d-105">Impone a un controllo Rich Edit di inviare un codice di notifica [**en \_ REQUESTRESIZE**](en-requestresize.md) alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="e579d-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="e579d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e579d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e579d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e579d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e579d-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e579d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e579d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e579d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e579d-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e579d-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e579d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e579d-111">Return value</span></span>

<span data-ttu-id="e579d-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e579d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e579d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e579d-113">Remarks</span></span>

<span data-ttu-id="e579d-114">Questo messaggio è utile durante l'elaborazione di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) per l'elemento padre di un controllo Rich Edit senza fondo.</span><span class="sxs-lookup"><span data-stu-id="e579d-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e579d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e579d-115">Requirements</span></span>



| <span data-ttu-id="e579d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e579d-116">Requirement</span></span> | <span data-ttu-id="e579d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e579d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e579d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e579d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e579d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e579d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e579d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e579d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e579d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e579d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e579d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e579d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e579d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e579d-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e579d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e579d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e579d-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e579d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e579d-126">**EN \_ REQUESTRESIZE**</span><span class="sxs-lookup"><span data-stu-id="e579d-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="e579d-127">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e579d-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e579d-128">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="e579d-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

