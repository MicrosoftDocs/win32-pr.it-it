---
title: Messaggio di WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: Il \_ \_ \_ messaggio VIDEOSOURCE di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può controllare l'origine video.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476222"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="3aeb8-104">\_ \_ Messaggio VIDEOSOURCE WM Cap DLG \_</span><span class="sxs-lookup"><span data-stu-id="3aeb8-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="3aeb8-105">Il messaggio **VIDEOSOURCE di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può controllare l'origine video.</span><span class="sxs-lookup"><span data-stu-id="3aeb8-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="3aeb8-106">La finestra di dialogo origine video potrebbe contenere controlli che selezionano origini di input; modificare la tonalità, il contrasto e la luminosità dell'immagine; e modificare la qualità del video prima di digitalizzare le immagini nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="3aeb8-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="3aeb8-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .</span><span class="sxs-lookup"><span data-stu-id="3aeb8-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="3aeb8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aeb8-108">Return Value</span></span>

<span data-ttu-id="3aeb8-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3aeb8-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aeb8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3aeb8-110">Remarks</span></span>

<span data-ttu-id="3aeb8-111">La finestra di dialogo origine video è univoca per ogni driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3aeb8-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="3aeb8-112">Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo di origine video.</span><span class="sxs-lookup"><span data-stu-id="3aeb8-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="3aeb8-113">Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoSource** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="3aeb8-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aeb8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aeb8-114">Requirements</span></span>



| <span data-ttu-id="3aeb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aeb8-115">Requirement</span></span> | <span data-ttu-id="3aeb8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3aeb8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3aeb8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aeb8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3aeb8-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aeb8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3aeb8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aeb8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3aeb8-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3aeb8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3aeb8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3aeb8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aeb8-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aeb8-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aeb8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aeb8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aeb8-124">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3aeb8-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3aeb8-125">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3aeb8-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





