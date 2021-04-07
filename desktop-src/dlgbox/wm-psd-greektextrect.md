---
title: Messaggio WM_PSD_GREEKTEXTRECT (COMMDLG. h)
description: Notifica alla procedura di hook di una finestra di dialogo di impostazione della pagina, PagePaintHook, che la finestra di dialogo sta per creare testo greco all'interno del rettangolo dei margini della pagina di esempio.
ms.assetid: ad0a200d-5626-4768-b3bd-73d4e3f0d548
keywords:
- Finestre di dialogo WM_PSD_GREEKTEXTRECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_GREEKTEXTRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0853720bea8cadc8df40d8fa649f644fd00694
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048567"
---
# <a name="wm_psd_greektextrect-message"></a><span data-ttu-id="f6a6e-104">\_ \_ Messaggio GREEKTEXTRECT di WM PSD</span><span class="sxs-lookup"><span data-stu-id="f6a6e-104">WM\_PSD\_GREEKTEXTRECT message</span></span>

<span data-ttu-id="f6a6e-105">Notifica alla procedura di hook di una finestra di dialogo di **impostazione della pagina** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per creare testo greco all'interno del rettangolo dei margini della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw Greek text inside the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_GREEKTEXTRECT    (WM_USER+4)
```



## <a name="parameters"></a><span data-ttu-id="f6a6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6a6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6a6e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a6e-108">Handle per il contesto di dispositivo per la pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="f6a6e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6a6e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a6e-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo di testo greco.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the Greek text rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a6e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6a6e-111">Return value</span></span>

<span data-ttu-id="f6a6e-112">Se la procedura di hook restituisce **true**, nella finestra di dialogo non viene disegnato il testo greco della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-112">If the hook procedure returns **TRUE**, the dialog box does not draw the Greek text portion of the sample page.</span></span>

<span data-ttu-id="f6a6e-113">Se la procedura di hook restituisce **false**, nella finestra di dialogo viene disegnata la parte di testo in greco della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-113">If the hook procedure returns **FALSE**, the dialog box draws the Greek text portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a6e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6a6e-114">Remarks</span></span>

<span data-ttu-id="f6a6e-115">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="f6a6e-116">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="f6a6e-117">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="f6a6e-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a6e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6a6e-118">Requirements</span></span>



| <span data-ttu-id="f6a6e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a6e-119">Requirement</span></span> | <span data-ttu-id="f6a6e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f6a6e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a6e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6a6e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a6e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6a6e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f6a6e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6a6e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a6e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6a6e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6a6e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6a6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6a6e-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6a6e-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a6e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6a6e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6a6e-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f6a6e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6a6e-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="f6a6e-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="f6a6e-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6a6e-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6a6e-131">**\_PAGESETUPDLG PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="f6a6e-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="f6a6e-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f6a6e-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6a6e-133">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="f6a6e-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

