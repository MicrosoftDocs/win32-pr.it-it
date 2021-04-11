---
title: Messaggio WM_CTLCOLORLISTBOX (winuser. h)
description: Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo. Rispondendo a questo messaggio, la finestra padre può impostare il testo e i colori di sfondo della casella di riepilogo usando l'handle del contesto del dispositivo di visualizzazione specificato.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Controlli di Windows Message WM_CTLCOLORLISTBOX
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119654"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="72e90-105">\_Messaggio CTLCOLORLISTBOX WM</span><span class="sxs-lookup"><span data-stu-id="72e90-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="72e90-106">Inviato alla finestra padre di una casella di riepilogo prima che il sistema disegni la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72e90-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="72e90-107">Rispondendo a questo messaggio, la finestra padre può impostare il testo e i colori di sfondo della casella di riepilogo usando l'handle del contesto del dispositivo di visualizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="72e90-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="72e90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="72e90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e90-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72e90-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72e90-110">Handle per il contesto di dispositivo per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72e90-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="72e90-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72e90-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72e90-112">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72e90-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72e90-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72e90-113">Return value</span></span>

<span data-ttu-id="72e90-114">Se un'applicazione elabora il messaggio, deve restituire un handle a un pennello.</span><span class="sxs-lookup"><span data-stu-id="72e90-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="72e90-115">Il sistema utilizza il pennello per disegnare lo sfondo della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72e90-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="72e90-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="72e90-116">Remarks</span></span>

<span data-ttu-id="72e90-117">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleziona i colori di sistema predefiniti per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="72e90-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="72e90-118">Il messaggio **WM \_ CTLCOLORLISTBOX** non viene mai inviato tra i thread.</span><span class="sxs-lookup"><span data-stu-id="72e90-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="72e90-119">Viene inviato solo all'interno di un thread.</span><span class="sxs-lookup"><span data-stu-id="72e90-119">It is sent only within one thread.</span></span>

<span data-ttu-id="72e90-120">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **\_ ptr int** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="72e90-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="72e90-121">Se la routine della finestra di dialogo restituisce **false**, viene eseguita la gestione dei messaggi predefinita.</span><span class="sxs-lookup"><span data-stu-id="72e90-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="72e90-122">Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="72e90-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e90-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72e90-123">Requirements</span></span>



| <span data-ttu-id="72e90-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e90-124">Requirement</span></span> | <span data-ttu-id="72e90-125">Valore</span><span class="sxs-lookup"><span data-stu-id="72e90-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e90-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72e90-126">Minimum supported client</span></span><br/> | <span data-ttu-id="72e90-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72e90-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="72e90-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72e90-128">Minimum supported server</span></span><br/> | <span data-ttu-id="72e90-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72e90-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72e90-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72e90-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="72e90-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72e90-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e90-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72e90-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="72e90-133">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="72e90-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="72e90-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="72e90-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="72e90-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="72e90-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="72e90-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="72e90-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

