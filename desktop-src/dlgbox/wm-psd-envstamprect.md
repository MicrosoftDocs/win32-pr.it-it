---
title: Messaggio WM_PSD_ENVSTAMPRECT (COMMDLG. h)
description: Notifica alla procedura di hook di una finestra di dialogo di impostazione della pagina, PagePaintHook, che la finestra di dialogo sta per creare il rettangolo del timbro della busta della pagina di esempio.
ms.assetid: f193baa0-a084-416e-90c9-9c838758a3d3
keywords:
- Finestre di dialogo WM_PSD_ENVSTAMPRECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_ENVSTAMPRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf13485ab75f51298ef273c7e02ea0253e4244d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477969"
---
# <a name="wm_psd_envstamprect-message"></a><span data-ttu-id="3aa23-104">\_ \_ Messaggio ENVSTAMPRECT di WM PSD</span><span class="sxs-lookup"><span data-stu-id="3aa23-104">WM\_PSD\_ENVSTAMPRECT message</span></span>

<span data-ttu-id="3aa23-105">Notifica alla procedura di hook di una finestra di dialogo di **impostazione della pagina** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per creare il rettangolo del timbro della busta della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="3aa23-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the envelope-stamp rectangle of the sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_ENVSTAMPRECT     (WM_USER+5)
```



## <a name="parameters"></a><span data-ttu-id="3aa23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aa23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa23-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3aa23-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa23-108">Handle per il contesto di dispositivo per la pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="3aa23-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="3aa23-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3aa23-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3aa23-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, del rettangolo del timbro della busta.</span><span class="sxs-lookup"><span data-stu-id="3aa23-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the envelope-stamp rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa23-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aa23-111">Return value</span></span>

<span data-ttu-id="3aa23-112">Se la procedura di hook restituisce **true**, nella finestra di dialogo non viene creata la parte relativa al timbro della busta della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="3aa23-112">If the hook procedure returns **TRUE**, the dialog box does not draw the envelope-stamp portion of the sample page.</span></span>

<span data-ttu-id="3aa23-113">Se la routine hook restituisce **false**, nella finestra di dialogo viene disegnata la parte relativa all'impronta della busta della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="3aa23-113">If the hook procedure returns **FALSE**, the dialog box draws the envelope-stamp portion of the sample page.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa23-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3aa23-114">Remarks</span></span>

<span data-ttu-id="3aa23-115">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="3aa23-115">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="3aa23-116">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="3aa23-116">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="3aa23-117">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="3aa23-117">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

<span data-ttu-id="3aa23-118">Una routine hook riceve questo messaggio solo se il tipo di carta selezionato è una busta.</span><span class="sxs-lookup"><span data-stu-id="3aa23-118">A hook procedure receives this message only if the selected paper type is an envelope.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa23-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aa23-119">Requirements</span></span>



| <span data-ttu-id="3aa23-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa23-120">Requirement</span></span> | <span data-ttu-id="3aa23-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3aa23-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa23-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aa23-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa23-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aa23-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3aa23-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aa23-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa23-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aa23-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3aa23-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3aa23-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa23-127"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa23-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa23-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aa23-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3aa23-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3aa23-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3aa23-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="3aa23-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="3aa23-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3aa23-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3aa23-132">**\_PAGESETUPDLG PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="3aa23-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="3aa23-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3aa23-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3aa23-134">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="3aa23-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

