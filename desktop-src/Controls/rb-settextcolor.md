---
title: Messaggio RB_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo predefinito del controllo Rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Controlli di Windows Message RB_SETTEXTCOLOR
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477860"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="53e4b-104">\_Messaggio SETTEXTCOLOR RB</span><span class="sxs-lookup"><span data-stu-id="53e4b-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="53e4b-105">Imposta il colore del testo predefinito del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="53e4b-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="53e4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e4b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53e4b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53e4b-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="53e4b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="53e4b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53e4b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53e4b-110">Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il nuovo colore del testo predefinito.</span><span class="sxs-lookup"><span data-stu-id="53e4b-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e4b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53e4b-111">Return value</span></span>

<span data-ttu-id="53e4b-112">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore del testo predefinito precedente.</span><span class="sxs-lookup"><span data-stu-id="53e4b-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e4b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="53e4b-113">Remarks</span></span>

<span data-ttu-id="53e4b-114">Il colore del testo predefinito del controllo Rebar viene utilizzato per creare il testo in un controllo Rebar e tutte le bande aggiunte dopo l'invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53e4b-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="53e4b-115">Il colore del testo predefinito per una particolare banda può essere sottoposto a override quando si aggiunge o si modifica una banda impostando il \_ flag RBBIM Colors in **fmask** e impostando **clrBack** nella struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .</span><span class="sxs-lookup"><span data-stu-id="53e4b-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e4b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53e4b-116">Requirements</span></span>



| <span data-ttu-id="53e4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="53e4b-117">Requirement</span></span> | <span data-ttu-id="53e4b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="53e4b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53e4b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53e4b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53e4b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53e4b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53e4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53e4b-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53e4b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53e4b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53e4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53e4b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53e4b-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e4b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53e4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e4b-126">**RB \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="53e4b-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

