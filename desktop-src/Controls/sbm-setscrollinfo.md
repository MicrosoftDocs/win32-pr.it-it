---
title: Messaggio SBM_SETSCROLLINFO (winuser. h)
description: Il \_ messaggio SETSCROLLINFO SBM viene inviato per impostare i parametri di una barra di scorrimento.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Controlli di Windows Message SBM_SETSCROLLINFO
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302128"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="66efe-104">\_Messaggio SETSCROLLINFO SBM</span><span class="sxs-lookup"><span data-stu-id="66efe-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="66efe-105">Il **messaggio \_ SETSCROLLINFO SBM** viene inviato per impostare i parametri di una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="66efe-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="66efe-106">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="66efe-106">Applications should not send this message directly.</span></span> <span data-ttu-id="66efe-107">Devono invece usare la funzione [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="66efe-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="66efe-108">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="66efe-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="66efe-109">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollInfo** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="66efe-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="66efe-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="66efe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66efe-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66efe-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66efe-112">Specifica se la barra di scorrimento viene ridisegnato per riflettere la nuova posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="66efe-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="66efe-113">Se questo parametro è **true**, la barra di scorrimento viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="66efe-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="66efe-114">Se è **false**, la barra di scorrimento non viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="66efe-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="66efe-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66efe-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66efe-116">Puntatore a una struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="66efe-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="66efe-117">Prima di chiamare [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), impostare il membro **cbSize** della struttura su **sizeof**(**ScrollInfo**), impostare il membro **fmask** per indicare i parametri da impostare e specificare i nuovi valori dei parametri nei membri appropriati.</span><span class="sxs-lookup"><span data-stu-id="66efe-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="66efe-118">Il membro **fmask** può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="66efe-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="66efe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="66efe-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="66efe-120">Significato</span><span class="sxs-lookup"><span data-stu-id="66efe-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="66efe-121"><dt>**\_DISABLENOSCROLL sif**</dt></span><span class="sxs-lookup"><span data-stu-id="66efe-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="66efe-122">Disabilita la barra di scorrimento anziché rimuoverla, se i nuovi parametri della barra di scorrimento rendono superflua la barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="66efe-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="66efe-123"><dt>**\_pagina sif**</dt></span><span class="sxs-lookup"><span data-stu-id="66efe-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="66efe-124">Imposta la pagina di scorrimento sul valore specificato nel membro **nPage** .</span><span class="sxs-lookup"><span data-stu-id="66efe-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="66efe-125"><dt>**SIF \_ pos**</dt></span><span class="sxs-lookup"><span data-stu-id="66efe-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="66efe-126">Imposta la posizione di scorrimento sul valore specificato nel membro **nPos** .</span><span class="sxs-lookup"><span data-stu-id="66efe-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="66efe-127"><dt>**\_intervallo sif**</dt></span><span class="sxs-lookup"><span data-stu-id="66efe-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="66efe-128">Imposta l'intervallo di scorrimento sul valore specificato nei membri **nmin** e **nmax** .</span><span class="sxs-lookup"><span data-stu-id="66efe-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66efe-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66efe-129">Return value</span></span>

<span data-ttu-id="66efe-130">Il valore restituito è la posizione corrente della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="66efe-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="66efe-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="66efe-131">Remarks</span></span>

<span data-ttu-id="66efe-132">I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md), forniscono solo 16 bit di dati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="66efe-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="66efe-133">Tuttavia, la struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit dei dati relativi alla posizione della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="66efe-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="66efe-134">È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere i dati relativi alla posizione della barra di scorrimento a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="66efe-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="66efe-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66efe-135">Requirements</span></span>



| <span data-ttu-id="66efe-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="66efe-136">Requirement</span></span> | <span data-ttu-id="66efe-137">Valore</span><span class="sxs-lookup"><span data-stu-id="66efe-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66efe-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66efe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="66efe-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66efe-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66efe-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66efe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="66efe-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66efe-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66efe-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66efe-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="66efe-143"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66efe-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66efe-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66efe-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="66efe-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="66efe-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66efe-146">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="66efe-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="66efe-147">**\_GETSCROLLINFO SBM**</span><span class="sxs-lookup"><span data-stu-id="66efe-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="66efe-148">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="66efe-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="66efe-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="66efe-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

