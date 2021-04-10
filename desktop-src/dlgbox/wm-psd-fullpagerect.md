---
title: Messaggio WM_PSD_FULLPAGERECT (COMMDLG. h)
description: Notifica a una procedura di hook PagePaintHook le coordinate del rettangolo della pagina di esempio nella finestra di dialogo Imposta pagina. La finestra di dialogo Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- Finestre di dialogo WM_PSD_FULLPAGERECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5265144822ba1f46c470b71169e0b27f2e1c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964595"
---
# <a name="wm_psd_fullpagerect-message"></a><span data-ttu-id="2a39b-105">\_ \_ Messaggio FULLPAGERECT di WM PSD</span><span class="sxs-lookup"><span data-stu-id="2a39b-105">WM\_PSD\_FULLPAGERECT message</span></span>

<span data-ttu-id="2a39b-106">Notifica a una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) le coordinate del rettangolo della pagina di esempio nella finestra di dialogo **Imposta pagina** .</span><span class="sxs-lookup"><span data-stu-id="2a39b-106">Notifies a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure of the coordinates of the sample page rectangle in the **Page Setup** dialog box.</span></span> <span data-ttu-id="2a39b-107">La finestra di dialogo Invia questo messaggio quando sta per essere disegnato il contenuto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="2a39b-107">The dialog box sends this message when it is about to draw the contents of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="2a39b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a39b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a39b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a39b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a39b-110">Handle per il contesto di dispositivo per la pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="2a39b-110">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="2a39b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a39b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a39b-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="2a39b-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a39b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a39b-113">Return value</span></span>

<span data-ttu-id="2a39b-114">Se la procedura di hook restituisce **true**, la finestra di dialogo non invia più messaggi e non viene disegnato nella pagina di esempio fino alla successiva necessità di ricreare la pagina di esempio dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2a39b-114">If the hook procedure returns **TRUE**, the dialog box sends no more messages and does not draw in the sample page until the next time the system needs to redraw the sample page.</span></span>

<span data-ttu-id="2a39b-115">Se la routine hook restituisce **false**, la finestra di dialogo Invia i messaggi rimanenti della sequenza di disegno.</span><span class="sxs-lookup"><span data-stu-id="2a39b-115">If the hook procedure returns **FALSE**, the dialog box sends the remaining messages of the drawing sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a39b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a39b-116">Remarks</span></span>

<span data-ttu-id="2a39b-117">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="2a39b-117">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="2a39b-118">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="2a39b-118">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="2a39b-119">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="2a39b-119">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a39b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a39b-120">Requirements</span></span>



| <span data-ttu-id="2a39b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a39b-121">Requirement</span></span> | <span data-ttu-id="2a39b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2a39b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a39b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a39b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2a39b-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a39b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a39b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a39b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2a39b-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a39b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a39b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a39b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a39b-128"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a39b-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a39b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a39b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a39b-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2a39b-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a39b-131">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="2a39b-131">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="2a39b-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a39b-132">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2a39b-133">**\_PAGESETUPDLG PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="2a39b-133">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="2a39b-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2a39b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a39b-135">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="2a39b-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

