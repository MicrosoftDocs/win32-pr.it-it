---
title: Messaggio WM_PSD_MARGINRECT (COMMDLG. h)
description: Notifica alla procedura di hook di una finestra di dialogo di impostazione della pagina, PagePaintHook, che la finestra di dialogo sta per creare il rettangolo dei margini della pagina di esempio.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- Finestre di dialogo WM_PSD_MARGINRECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718cfbe16db53378544d9fca0ab44ade23ffb3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477968"
---
# <a name="wm_psd_marginrect-message"></a><span data-ttu-id="e8099-104">\_ \_ Messaggio MARGINRECT di WM PSD</span><span class="sxs-lookup"><span data-stu-id="e8099-104">WM\_PSD\_MARGINRECT message</span></span>

<span data-ttu-id="e8099-105">Notifica alla procedura di hook di una finestra di dialogo di **impostazione della pagina** , [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per creare il rettangolo dei margini della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="e8099-105">Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the margin rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## <a name="parameters"></a><span data-ttu-id="e8099-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8099-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8099-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8099-108">Handle per il contesto di dispositivo per la pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="e8099-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="e8099-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8099-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8099-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del margine.</span><span class="sxs-lookup"><span data-stu-id="e8099-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the margin rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8099-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8099-111">Return value</span></span>

<span data-ttu-id="e8099-112">Se la procedura di hook restituisce **true**, nella finestra di dialogo non viene disegnato il rettangolo dei margini nella pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="e8099-112">If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.</span></span>

<span data-ttu-id="e8099-113">Se la routine hook restituisce **false**, nella finestra di dialogo viene disegnato il rettangolo dei margini nella pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="e8099-113">If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8099-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8099-114">Remarks</span></span>

<span data-ttu-id="e8099-115">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="e8099-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="e8099-116">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="e8099-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="e8099-117">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="e8099-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8099-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8099-118">Requirements</span></span>



| <span data-ttu-id="e8099-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8099-119">Requirement</span></span> | <span data-ttu-id="e8099-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e8099-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8099-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8099-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8099-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8099-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e8099-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8099-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8099-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8099-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8099-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8099-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8099-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8099-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8099-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8099-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8099-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e8099-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e8099-129">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="e8099-129">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="e8099-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8099-130">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e8099-131">**\_PAGESETUPDLG PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="e8099-131">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="e8099-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e8099-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e8099-133">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="e8099-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

