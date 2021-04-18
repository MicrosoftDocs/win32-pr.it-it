---
title: Messaggio WM_INITDIALOG (winuser. h)
description: Inviato alla routine della finestra di dialogo immediatamente prima della visualizzazione di una finestra di dialogo. Le routine della finestra di dialogo utilizzano in genere questo messaggio per inizializzare i controlli e per eseguire altre attività di inizializzazione che influiscono sull'aspetto della finestra di dialogo.
ms.assetid: bc4f4718-1dab-48db-ae3b-5a81a7be2644
keywords:
- Finestre di dialogo WM_INITDIALOG messaggio
topic_type:
- apiref
api_name:
- WM_INITDIALOG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64646075bc3d5c90076d6c1ca0d61f80111c90ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302082"
---
# <a name="wm_initdialog-message"></a><span data-ttu-id="606cf-105">\_Messaggio INITDIALOG WM</span><span class="sxs-lookup"><span data-stu-id="606cf-105">WM\_INITDIALOG message</span></span>

<span data-ttu-id="606cf-106">Inviato alla routine della finestra di dialogo immediatamente prima della visualizzazione di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="606cf-106">Sent to the dialog box procedure immediately before a dialog box is displayed.</span></span> <span data-ttu-id="606cf-107">Le routine della finestra di dialogo utilizzano in genere questo messaggio per inizializzare i controlli e per eseguire altre attività di inizializzazione che influiscono sull'aspetto della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="606cf-107">Dialog box procedures typically use this message to initialize controls and carry out any other initialization tasks that affect the appearance of the dialog box.</span></span>


```C++
#define WM_INITDIALOG                   0x0110
```



## <a name="parameters"></a><span data-ttu-id="606cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="606cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="606cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="606cf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="606cf-110">Handle per il controllo per ricevere lo stato attivo della tastiera predefinito.</span><span class="sxs-lookup"><span data-stu-id="606cf-110">A handle to the control to receive the default keyboard focus.</span></span> <span data-ttu-id="606cf-111">Il sistema assegna lo stato attivo della tastiera predefinito solo se la routine della finestra di dialogo restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="606cf-111">The system assigns the default keyboard focus only if the dialog box procedure returns **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="606cf-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="606cf-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="606cf-113">Dati di inizializzazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="606cf-113">Additional initialization data.</span></span> <span data-ttu-id="606cf-114">Questi dati vengono passati al sistema come parametro *lParam* in una chiamata alla funzione [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)o [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) usata per creare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="606cf-114">This data is passed to the system as the *lParam* parameter in a call to the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), or [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) function used to create the dialog box.</span></span> <span data-ttu-id="606cf-115">Per le finestre delle proprietà, questo parametro è un puntatore alla struttura [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) usata per creare la pagina.</span><span class="sxs-lookup"><span data-stu-id="606cf-115">For property sheets, this parameter is a pointer to the [**PROPSHEETPAGE**](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2) structure used to create the page.</span></span> <span data-ttu-id="606cf-116">Questo parametro è zero se viene utilizzata un'altra funzione di creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="606cf-116">This parameter is zero if any other dialog box creation function is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="606cf-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="606cf-117">Return value</span></span>

<span data-ttu-id="606cf-118">La routine della finestra di dialogo deve restituire **true** per indirizzare il sistema in modo da impostare lo stato attivo sulla tastiera sul controllo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="606cf-118">The dialog box procedure should return **TRUE** to direct the system to set the keyboard focus to the control specified by *wParam*.</span></span> <span data-ttu-id="606cf-119">In caso contrario, deve restituire **false** per impedire che il sistema imposti lo stato attivo della tastiera predefinito.</span><span class="sxs-lookup"><span data-stu-id="606cf-119">Otherwise, it should return **FALSE** to prevent the system from setting the default keyboard focus.</span></span>

<span data-ttu-id="606cf-120">La routine della finestra di dialogo deve restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="606cf-120">The dialog box procedure should return the value directly.</span></span> <span data-ttu-id="606cf-121">Il valore **DWL \_ MSGRESULT** impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="606cf-121">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="606cf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="606cf-122">Remarks</span></span>

<span data-ttu-id="606cf-123">Il controllo che riceve lo stato attivo predefinito è sempre il primo controllo nella finestra di dialogo visibile, non disabilitato e con lo stile **WS \_ TABSTOP** .</span><span class="sxs-lookup"><span data-stu-id="606cf-123">The control to receive the default keyboard focus is always the first control in the dialog box that is visible, not disabled, and that has the **WS\_TABSTOP** style.</span></span> <span data-ttu-id="606cf-124">Quando la routine della finestra di dialogo restituisce **true**, il sistema controlla il controllo per verificare che la procedura non sia stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="606cf-124">When the dialog box procedure returns **TRUE**, the system checks the control to ensure that the procedure has not disabled it.</span></span> <span data-ttu-id="606cf-125">Se è stato disabilitato, il sistema imposta lo stato attivo della tastiera sul controllo successivo visibile, non disabilitato e con **WS \_ TABSTOP**.</span><span class="sxs-lookup"><span data-stu-id="606cf-125">If it has been disabled, the system sets the keyboard focus to the next control that is visible, not disabled, and has the **WS\_TABSTOP**.</span></span>

<span data-ttu-id="606cf-126">Un'applicazione può restituire **false** solo se ha impostato lo stato attivo su uno dei controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="606cf-126">An application can return **FALSE** only if it has set the keyboard focus to one of the controls of the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="606cf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="606cf-127">Requirements</span></span>



| <span data-ttu-id="606cf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="606cf-128">Requirement</span></span> | <span data-ttu-id="606cf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="606cf-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="606cf-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="606cf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="606cf-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="606cf-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="606cf-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="606cf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="606cf-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="606cf-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="606cf-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="606cf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="606cf-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="606cf-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="606cf-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="606cf-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="606cf-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="606cf-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="606cf-138">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="606cf-138">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="606cf-139">**CreateDialogParam**</span><span class="sxs-lookup"><span data-stu-id="606cf-139">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
</dt> <dt>

[<span data-ttu-id="606cf-140">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="606cf-140">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="606cf-141">**DialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="606cf-141">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
</dt> <dt>

[<span data-ttu-id="606cf-142">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="606cf-142">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="606cf-143">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="606cf-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="606cf-144">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="606cf-144">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="606cf-145">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="606cf-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="606cf-146">**PROPSHEETPAGE**</span><span class="sxs-lookup"><span data-stu-id="606cf-146">**PROPSHEETPAGE**</span></span>](/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2)
</dt> </dl>

 

