---
title: Messaggio WM_DWMSENDICONICLIVEPREVIEWBITMAP (dwmapi. h)
description: Indica a una finestra di fornire una bitmap statica da utilizzare come anteprima in tempo reale (nota anche come anteprima di visualizzazione) di tale finestra.
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- Messaggio WM_DWMSENDICONICLIVEPREVIEWBITMAP Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477002"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="2db28-104">\_Messaggio DWMSENDICONICLIVEPREVIEWBITMAP WM</span><span class="sxs-lookup"><span data-stu-id="2db28-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="2db28-105">Indica a una finestra di fornire una bitmap statica da utilizzare come *anteprima in tempo reale* (nota anche come *Anteprima di visualizzazione*) di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="2db28-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2db28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2db28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2db28-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2db28-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2db28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2db28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2db28-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2db28-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db28-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2db28-111">Return value</span></span>

<span data-ttu-id="2db28-112">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="2db28-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db28-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2db28-113">Remarks</span></span>

<span data-ttu-id="2db28-114">Un' *anteprima in tempo reale* , nota anche come *Anteprima* di una finestra, viene visualizzata quando un utente sposta il puntatore del mouse sull'anteprima della finestra nella barra delle applicazioni o assegna all'anteprima lo stato attivo nella finestra Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="2db28-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="2db28-115">Questa vista è un'anteprima completa della finestra e può essere uno snapshot Live o una rappresentazione iconica.</span><span class="sxs-lookup"><span data-stu-id="2db28-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="2db28-116">Gestione finestre desktop (DWM) Invia questo messaggio a una finestra se si verificano tutte le situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2db28-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="2db28-117">L'anteprima in tempo reale è stata richiamata nella finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="2db28-118">Per DWMWA è impostato un attributo [**\_ \_ \_ bitmap iconico**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) nella finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="2db28-119">Una rappresentazione iconica è l'unica esistente per questa finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="2db28-120">La finestra che riceve questo messaggio deve rispondere generando una bitmap a scalabilità totale.</span><span class="sxs-lookup"><span data-stu-id="2db28-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="2db28-121">La finestra chiama quindi la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) per impostare l'anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="2db28-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="2db28-122">Se la finestra non imposta una bitmap in un determinato periodo di tempo, DWM utilizza la propria rappresentazione iconica predefinita per la finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="2db28-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="2db28-123">Examples</span></span>

<span data-ttu-id="2db28-124">Nell'esempio seguente viene illustrata una risposta al messaggio **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** .</span><span class="sxs-lookup"><span data-stu-id="2db28-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="2db28-125">L'esempio chiama la funzione [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) con un handle per una bitmap personalizzata, indipendente dal dispositivo, da usare come rappresentazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="2db28-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="2db28-126">Per il codice completo, vedere l'esempio [personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="2db28-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db28-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2db28-127">Requirements</span></span>



| <span data-ttu-id="2db28-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db28-128">Requirement</span></span> | <span data-ttu-id="2db28-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2db28-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2db28-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db28-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2db28-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2db28-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2db28-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db28-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2db28-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2db28-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2db28-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2db28-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db28-135"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db28-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2db28-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2db28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db28-137">**\_DWMSENDICONICTHUMBNAIL WM**</span><span class="sxs-lookup"><span data-stu-id="2db28-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="2db28-138">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="2db28-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 





