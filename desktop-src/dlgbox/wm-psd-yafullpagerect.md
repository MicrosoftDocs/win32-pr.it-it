---
title: Messaggio WM_PSD_YAFULLPAGERECT (COMMDLG. h)
description: Notifica alla procedura hook di una finestra di dialogo di impostazione della pagina, PagePaintHook, che la finestra di dialogo sta per creare la parte dell'indirizzo mittente di una pagina di esempio della busta.
ms.assetid: 1f6aea69-a1bd-41ea-b508-44b4f5c38757
keywords:
- Finestre di dialogo WM_PSD_YAFULLPAGERECT messaggio
topic_type:
- apiref
api_name:
- WM_PSD_YAFULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb325a8d408724cd865f5f9b70cfe7369fe6ffe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048717"
---
# <a name="wm_psd_yafullpagerect-message"></a><span data-ttu-id="0d433-104">\_ \_ Messaggio YAFULLPAGERECT di WM PSD</span><span class="sxs-lookup"><span data-stu-id="0d433-104">WM\_PSD\_YAFULLPAGERECT message</span></span>

<span data-ttu-id="0d433-105">Notifica alla procedura hook di una finestra di dialogo di **impostazione della pagina** , [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), che la finestra di dialogo sta per creare la parte dell'indirizzo mittente di una pagina di esempio della busta.</span><span class="sxs-lookup"><span data-stu-id="0d433-105">Notifies the hook procedure of a **Page Setup** dialog box, [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook), that the dialog box is about to draw the return address portion of an envelope sample page.</span></span>


```C++
#define WM_USER                  0x0400
#define WM_PSD_YAFULLPAGERECT   (WM_USER+6)
```



## <a name="parameters"></a><span data-ttu-id="0d433-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d433-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d433-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d433-108">Handle per il contesto di dispositivo per la pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="0d433-108">A handle to the device context for the sample page.</span></span>

</dd> <dt>

<span data-ttu-id="0d433-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d433-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d433-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le coordinate, in pixel, della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="0d433-110">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the coordinates, in pixels, of the sample page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d433-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d433-111">Return value</span></span>

<span data-ttu-id="0d433-112">Se la procedura di hook restituisce **true**, nella finestra di dialogo non viene creata la parte relativa all'indirizzo di restituzione di una pagina di esempio della busta.</span><span class="sxs-lookup"><span data-stu-id="0d433-112">If the hook procedure returns **TRUE**, the dialog box does not draw the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="0d433-113">Se la routine hook restituisce **false**, nella finestra di dialogo viene disegnata la parte dell'indirizzo restituito di una pagina di esempio della busta.</span><span class="sxs-lookup"><span data-stu-id="0d433-113">If the hook procedure returns **FALSE**, the dialog box draws the return address portion of an envelope sample page.</span></span>

<span data-ttu-id="0d433-114">Se il tipo di carta non è una busta, il valore restituito non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0d433-114">If the paper type is not an envelope, the return value has no effect.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d433-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d433-115">Remarks</span></span>

<span data-ttu-id="0d433-116">Nella finestra di dialogo **Imposta pagina** è inclusa un'immagine di una pagina di esempio in cui viene illustrato il modo in cui le selezioni dell'utente influiscono sull'aspetto dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="0d433-116">The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output.</span></span> <span data-ttu-id="0d433-117">Quando si chiama la funzione [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , è possibile fornire una procedura di hook [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) per personalizzare l'aspetto della pagina di esempio.</span><span class="sxs-lookup"><span data-stu-id="0d433-117">When you call the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function, you can provide a [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize the appearance of the sample page.</span></span> <span data-ttu-id="0d433-118">Ogni volta che la finestra di dialogo sta per creare il contenuto della pagina di esempio, la finestra di dialogo Invia una sequenza di messaggi alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="0d433-118">Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d433-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d433-119">Requirements</span></span>



| <span data-ttu-id="0d433-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d433-120">Requirement</span></span> | <span data-ttu-id="0d433-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0d433-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d433-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d433-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d433-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d433-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0d433-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d433-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d433-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d433-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d433-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d433-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d433-127"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d433-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d433-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d433-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d433-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0d433-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d433-130">*PagePaintHook*</span><span class="sxs-lookup"><span data-stu-id="0d433-130">*PagePaintHook*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

<span data-ttu-id="0d433-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0d433-131">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0d433-132">**\_PAGESETUPDLG PSD \_ WM**</span><span class="sxs-lookup"><span data-stu-id="0d433-132">**WM\_PSD\_PAGESETUPDLG**</span></span>](wm-psd-pagesetupdlg.md)
</dt> <dt>

<span data-ttu-id="0d433-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0d433-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0d433-134">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="0d433-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

