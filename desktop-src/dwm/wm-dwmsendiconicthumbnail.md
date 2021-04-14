---
title: Messaggio WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Messaggio WM_DWMSENDICONICTHUMBNAIL Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478766"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="afbd6-104">\_Messaggio DWMSENDICONICTHUMBNAIL WM</span><span class="sxs-lookup"><span data-stu-id="afbd6-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="afbd6-105">Indica a una finestra di fornire una bitmap statica da utilizzare come rappresentazione di anteprima di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="afbd6-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="afbd6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="afbd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afbd6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afbd6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afbd6-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="afbd6-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="afbd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afbd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afbd6-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo valore è la coordinata x massima dell'anteprima.</span><span class="sxs-lookup"><span data-stu-id="afbd6-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="afbd6-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la coordinata y massima.</span><span class="sxs-lookup"><span data-stu-id="afbd6-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="afbd6-112">Se un'anteprima ha una dimensione che supera uno o entrambi questi valori, DWM non accetta l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="afbd6-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afbd6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afbd6-113">Return value</span></span>

<span data-ttu-id="afbd6-114">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="afbd6-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="afbd6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="afbd6-115">Remarks</span></span>

<span data-ttu-id="afbd6-116">DWM Invia questo messaggio a una finestra se si verificano tutte le situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="afbd6-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="afbd6-117">DWM Visualizza una rappresentazione iconica della finestra.</span><span class="sxs-lookup"><span data-stu-id="afbd6-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="afbd6-118">Per DWMWA è impostato un attributo [**\_ \_ \_ bitmap iconico**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) nella finestra.</span><span class="sxs-lookup"><span data-stu-id="afbd6-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="afbd6-119">Nella finestra non è stata impostata una bitmap memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="afbd6-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="afbd6-120">Nella cache è presente spazio per un'altra bitmap.</span><span class="sxs-lookup"><span data-stu-id="afbd6-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="afbd6-121">La finestra che riceve questo messaggio deve rispondere generando una bitmap che non è più grande della dimensione richiesta nei parametri del messaggio.</span><span class="sxs-lookup"><span data-stu-id="afbd6-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="afbd6-122">La finestra chiama quindi la funzione [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) per eseguire l'override dell'anteprima predefinita.</span><span class="sxs-lookup"><span data-stu-id="afbd6-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="afbd6-123">Se la finestra non fornisce una bitmap in un determinato periodo di tempo, DWM usa la propria rappresentazione iconica predefinita per la finestra.</span><span class="sxs-lookup"><span data-stu-id="afbd6-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="afbd6-124">La finestra deve appartenere al processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="afbd6-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="afbd6-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="afbd6-125">Examples</span></span>

<span data-ttu-id="afbd6-126">Nell'esempio di codice seguente viene illustrato come rispondere al messaggio **WM \_ DWMSENDICONICTHUMBNAIL** .</span><span class="sxs-lookup"><span data-stu-id="afbd6-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="afbd6-127">Nell'esempio viene chiamato [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)con un handle per una bitmap personalizzata indipendente dal dispositivo da utilizzare come rappresentazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="afbd6-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="afbd6-128">Per l'esempio completo, vedere l'esempio [personalizzare un'anteprima iconica e una bitmap di anteprima in tempo reale](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="afbd6-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="afbd6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afbd6-129">Requirements</span></span>



| <span data-ttu-id="afbd6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="afbd6-130">Requirement</span></span> | <span data-ttu-id="afbd6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="afbd6-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="afbd6-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afbd6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="afbd6-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="afbd6-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afbd6-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afbd6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="afbd6-135">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="afbd6-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afbd6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afbd6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="afbd6-137"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="afbd6-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afbd6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afbd6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afbd6-139">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="afbd6-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="afbd6-140">**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**</span><span class="sxs-lookup"><span data-stu-id="afbd6-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

