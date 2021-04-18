---
title: Messaggio RB_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo predefinito del controllo Rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Controlli di Windows Message RB_SETBKCOLOR
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301836"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="30332-104">\_Messaggio SETBKCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="30332-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="30332-105">Imposta il colore di sfondo predefinito del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="30332-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="30332-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30332-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30332-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="30332-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="30332-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="30332-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30332-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30332-110">Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il nuovo colore di sfondo predefinito.</span><span class="sxs-lookup"><span data-stu-id="30332-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30332-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30332-111">Return value</span></span>

<span data-ttu-id="30332-112">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore di sfondo predefinito precedente.</span><span class="sxs-lookup"><span data-stu-id="30332-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="30332-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="30332-113">Remarks</span></span>

<span data-ttu-id="30332-114">Il colore di sfondo predefinito del controllo Rebar viene utilizzato per creare lo sfondo in un controllo Rebar e tutte le bande aggiunte dopo l'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="30332-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="30332-115">Il colore di sfondo predefinito per una particolare banda può essere sottoposto a override quando si aggiunge o si modifica una banda impostando il \_ flag RBBIM Colors in **fmask** e impostando **clrBack** nella struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="30332-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="30332-116">Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="30332-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="30332-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30332-117">Requirements</span></span>



| <span data-ttu-id="30332-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30332-118">Requirement</span></span> | <span data-ttu-id="30332-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30332-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30332-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30332-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30332-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30332-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30332-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30332-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30332-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30332-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30332-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30332-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30332-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30332-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30332-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30332-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30332-127">**RB \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="30332-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

