---
description: Imposta il tipo di carattere che un controllo deve usare durante il disegno del testo.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Messaggio WM_SETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967562"
---
# <a name="wm_setfont-message"></a><span data-ttu-id="1d0dd-103">\_Messaggio del tipo di carattere WM</span><span class="sxs-lookup"><span data-stu-id="1d0dd-103">WM\_SETFONT message</span></span>

<span data-ttu-id="1d0dd-104">Imposta il tipo di carattere che un controllo deve usare durante il disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-104">Sets the font that a control is to use when drawing text.</span></span>


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a><span data-ttu-id="1d0dd-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d0dd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0dd-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d0dd-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d0dd-107">Handle per il tipo di carattere (**Hfont**).</span><span class="sxs-lookup"><span data-stu-id="1d0dd-107">A handle to the font (**HFONT**).</span></span> <span data-ttu-id="1d0dd-108">Se questo parametro è **null**, il controllo Usa il tipo di carattere di sistema predefinito per creare il testo.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-108">If this parameter is **NULL**, the control uses the default system font to draw text.</span></span>

</dd> <dt>

<span data-ttu-id="1d0dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d0dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d0dd-110">La parola di basso livello di *lParam* specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-110">The low-order word of *lParam* specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="1d0dd-111">Se questo parametro è **true**, il controllo viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-111">If this parameter is **TRUE**, the control redraws itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0dd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d0dd-112">Return value</span></span>

<span data-ttu-id="1d0dd-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-113">Type: **LRESULT**</span></span>

<span data-ttu-id="1d0dd-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0dd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d0dd-115">Remarks</span></span>

<span data-ttu-id="1d0dd-116">Il messaggio **WM di \_ tipo carattere** si applica a tutti i controlli, non solo alle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-116">The **WM\_SETFONT** message applies to all controls, not just those in dialog boxes.</span></span>

<span data-ttu-id="1d0dd-117">Il momento migliore per il proprietario di un controllo finestra di dialogo per impostare il tipo di carattere del controllo è quando riceve il messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="1d0dd-117">The best time for the owner of a dialog box control to set the font of the control is when it receives the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span> <span data-ttu-id="1d0dd-118">L'applicazione deve chiamare la funzione [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) per eliminare il tipo di carattere quando non è più necessario. ad esempio, dopo l'eliminazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-118">The application should call the [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) function to delete the font when it is no longer needed; for example, after it destroys the control.</span></span>

<span data-ttu-id="1d0dd-119">Le dimensioni del controllo non cambiano in seguito alla ricezione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-119">The size of the control does not change as a result of receiving this message.</span></span> <span data-ttu-id="1d0dd-120">Per evitare di ritagliare il testo che non rientra nei limiti del controllo, l'applicazione deve correggere le dimensioni della finestra del controllo prima di impostare il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-120">To avoid clipping text that does not fit within the boundaries of the control, the application should correct the size of the control window before it sets the font.</span></span>

<span data-ttu-id="1d0dd-121">Quando in una finestra di dialogo viene utilizzato lo stile del [ \_ tipo di carattere DS](../dlgbox/about-dialog-boxes.md) per impostare il testo nei relativi controlli, il sistema invia il messaggio di **carattere di \_ tipo WM** alla routine della finestra di dialogo prima di creare i controlli.</span><span class="sxs-lookup"><span data-stu-id="1d0dd-121">When a dialog box uses the [DS\_SETFONT](../dlgbox/about-dialog-boxes.md) style to set the text in its controls, the system sends the **WM\_SETFONT** message to the dialog box procedure before it creates the controls.</span></span> <span data-ttu-id="1d0dd-122">Un'applicazione può creare una finestra di dialogo che contiene lo \_ stile del tipo di carattere DS chiamando una delle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d0dd-122">An application can create a dialog box that contains the DS\_SETFONT style by calling any of the following functions:</span></span>

-   [<span data-ttu-id="1d0dd-123">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-123">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="1d0dd-124">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-124">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="1d0dd-125">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-125">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="1d0dd-126">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-126">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a><span data-ttu-id="1d0dd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d0dd-127">Requirements</span></span>



| <span data-ttu-id="1d0dd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0dd-128">Requirement</span></span> | <span data-ttu-id="1d0dd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1d0dd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0dd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d0dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0dd-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d0dd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1d0dd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d0dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0dd-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d0dd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d0dd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d0dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d0dd-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d0dd-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0dd-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d0dd-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d0dd-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d0dd-138">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-138">**CreateDialogIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="1d0dd-139">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-139">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="1d0dd-140">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-140">**DialogBoxIndirect**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="1d0dd-141">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-141">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="1d0dd-142">**DLGTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-142">**DLGTEMPLATE**</span></span>](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[<span data-ttu-id="1d0dd-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-143">**MAKELPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="1d0dd-144">**\_tipo di carattere WM GetFont**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-144">**WM\_GETFONT**</span></span>](wm-getfont.md)
</dt> <dt>

[<span data-ttu-id="1d0dd-145">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-145">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> <dt>

<span data-ttu-id="1d0dd-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d0dd-147">Windows</span><span class="sxs-lookup"><span data-stu-id="1d0dd-147">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="1d0dd-148">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1d0dd-149">**DeleteObject**</span><span class="sxs-lookup"><span data-stu-id="1d0dd-149">**DeleteObject**</span></span>](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
