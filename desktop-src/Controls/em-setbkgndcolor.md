---
title: Messaggio di EM_SETBKGNDCOLOR (RichEdit. h)
description: Il \_ messaggio SETBKGNDCOLOR em imposta il colore di sfondo per un controllo Rich Edit.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Controlli di Windows Message EM_SETBKGNDCOLOR
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874361"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="68cc0-104">\_Messaggio SETBKGNDCOLOR em</span><span class="sxs-lookup"><span data-stu-id="68cc0-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="68cc0-105">Il **messaggio \_ SETBKGNDCOLOR em** imposta il colore di sfondo per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="68cc0-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="68cc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68cc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68cc0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68cc0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68cc0-108">Specifica se utilizzare il colore di sistema.</span><span class="sxs-lookup"><span data-stu-id="68cc0-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="68cc0-109">Se questo parametro è un valore diverso da zero, lo sfondo viene impostato sul colore di sistema dello sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="68cc0-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="68cc0-110">In caso contrario, lo sfondo viene impostato sul colore specificato.</span><span class="sxs-lookup"><span data-stu-id="68cc0-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="68cc0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68cc0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68cc0-112">Struttura [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il colore se *wParam* è zero.</span><span class="sxs-lookup"><span data-stu-id="68cc0-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="68cc0-113">Per generare un **COLORREF**, usare la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="68cc0-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68cc0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68cc0-114">Return value</span></span>

<span data-ttu-id="68cc0-115">Questo messaggio restituisce il colore di sfondo originale.</span><span class="sxs-lookup"><span data-stu-id="68cc0-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="68cc0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68cc0-116">Requirements</span></span>



| <span data-ttu-id="68cc0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68cc0-117">Requirement</span></span> | <span data-ttu-id="68cc0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="68cc0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68cc0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68cc0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68cc0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68cc0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68cc0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68cc0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68cc0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68cc0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68cc0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68cc0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68cc0-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="68cc0-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68cc0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68cc0-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="68cc0-126">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="68cc0-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="68cc0-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="68cc0-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="68cc0-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="68cc0-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

