---
title: Messaggio SBM_GETSCROLLINFO (winuser. h)
description: Il \_ messaggio GETSCROLLINFO SBM viene inviato per recuperare i parametri di una barra di scorrimento.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Controlli di Windows Message SBM_GETSCROLLINFO
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302640"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="05d51-104">\_Messaggio GETSCROLLINFO SBM</span><span class="sxs-lookup"><span data-stu-id="05d51-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="05d51-105">Il **messaggio \_ GETSCROLLINFO SBM** viene inviato per recuperare i parametri di una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="05d51-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="05d51-106">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="05d51-106">Applications should not send this message directly.</span></span> <span data-ttu-id="05d51-107">Devono invece usare la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="05d51-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="05d51-108">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="05d51-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="05d51-109">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollInfo** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="05d51-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="05d51-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="05d51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d51-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05d51-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05d51-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="05d51-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="05d51-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05d51-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05d51-114">Puntatore a una struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="05d51-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="05d51-115">Prima di chiamare [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), impostare il membro **cbSize** della struttura su **sizeof**(**ScrollInfo**) e impostare il membro **fmask** per specificare i parametri della barra di scorrimento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="05d51-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="05d51-116">Prima di restituire, il messaggio copia i parametri specificati nei membri appropriati della struttura.</span><span class="sxs-lookup"><span data-stu-id="05d51-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="05d51-117">Il membro **fmask** può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="05d51-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="05d51-118">Valore</span><span class="sxs-lookup"><span data-stu-id="05d51-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="05d51-119">Significato</span><span class="sxs-lookup"><span data-stu-id="05d51-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="05d51-120"><dt>**\_tutte le sfi**</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="05d51-121">Combinazione della \_ pagina sif, SIF \_ pos, SIF \_ Range e SIF \_ TRACKPOS.</span><span class="sxs-lookup"><span data-stu-id="05d51-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="05d51-122"><dt>**\_pagina sif**</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="05d51-123">Copia la pagina di scorrimento nel membro nPage.</span><span class="sxs-lookup"><span data-stu-id="05d51-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="05d51-124"><dt>**SIF \_ pos**</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="05d51-125">Copia la posizione di scorrimento nel membro nPos.</span><span class="sxs-lookup"><span data-stu-id="05d51-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="05d51-126"><dt>**\_intervallo sif**</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="05d51-127">Copia l'intervallo di scorrimento nei membri nMin e nMax.</span><span class="sxs-lookup"><span data-stu-id="05d51-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="05d51-128"><dt>**\_TRACKPOS sif**</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="05d51-129">Copia la posizione di rilevamento della casella di scorrimento corrente nel membro nTrackPos.</span><span class="sxs-lookup"><span data-stu-id="05d51-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d51-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05d51-130">Return value</span></span>

<span data-ttu-id="05d51-131">Se il messaggio recupera tutti i valori, il valore restituito è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="05d51-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d51-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="05d51-132">Remarks</span></span>

<span data-ttu-id="05d51-133">I messaggi che indicano la posizione della barra di scorrimento, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md), forniscono solo 16 bit di dati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="05d51-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="05d51-134">Tuttavia, la struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usata da **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornisce 32 bit dei dati relativi alla posizione della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="05d51-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="05d51-135">È possibile usare questi messaggi e funzioni durante l'elaborazione dei messaggi **WM \_ HSCROLL** o **WM \_ VSCROLL** per ottenere i dati relativi alla posizione della barra di scorrimento a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="05d51-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="05d51-136">Per ottenere la posizione a 32 bit della casella di scorrimento (Thumb) durante un \_ codice di richiesta SB THUMBTRACK in un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) , inviare **SBM \_ GETSCROLLINFO** con il \_ valore sif TRACKPOS nel membro **fmask** della struttura [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="05d51-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="05d51-137">Il messaggio restituisce la posizione di rilevamento della casella di scorrimento nel membro **nTrackPos** della struttura **ScrollInfo** .</span><span class="sxs-lookup"><span data-stu-id="05d51-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="05d51-138">Questo consente di ottenere la posizione della casella di scorrimento quando l'utente lo sposta.</span><span class="sxs-lookup"><span data-stu-id="05d51-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="05d51-139">In alternativa, è possibile usare la funzione [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) per ottenere le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="05d51-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d51-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05d51-140">Requirements</span></span>



| <span data-ttu-id="05d51-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d51-141">Requirement</span></span> | <span data-ttu-id="05d51-142">Valore</span><span class="sxs-lookup"><span data-stu-id="05d51-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d51-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05d51-143">Minimum supported client</span></span><br/> | <span data-ttu-id="05d51-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05d51-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="05d51-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05d51-145">Minimum supported server</span></span><br/> | <span data-ttu-id="05d51-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="05d51-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="05d51-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05d51-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d51-148"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05d51-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d51-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05d51-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="05d51-150">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="05d51-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05d51-151">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="05d51-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="05d51-152">**\_SETSCROLLINFO SBM**</span><span class="sxs-lookup"><span data-stu-id="05d51-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="05d51-153">**SCROLLINFO**</span><span class="sxs-lookup"><span data-stu-id="05d51-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="05d51-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="05d51-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

