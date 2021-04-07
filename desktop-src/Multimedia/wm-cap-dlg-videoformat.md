---
title: Messaggio di WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: Il \_ \_ \_ messaggio VIDEOFORMAT di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può selezionare il formato video.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964095"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="d3a1f-104">\_ \_ Messaggio VIDEOFORMAT WM Cap DLG \_</span><span class="sxs-lookup"><span data-stu-id="d3a1f-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="d3a1f-105">Il messaggio **VIDEOFORMAT di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può selezionare il formato video.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="d3a1f-106">La finestra di dialogo Formato video può essere usata per selezionare le dimensioni dell'immagine, la profondità dei bit e le opzioni di compressione hardware.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="d3a1f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="d3a1f-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="d3a1f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3a1f-108">Return Value</span></span>

<span data-ttu-id="d3a1f-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a1f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3a1f-110">Remarks</span></span>

<span data-ttu-id="d3a1f-111">Quando il messaggio viene restituito, le applicazioni potrebbero dover aggiornare la struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) perché l'utente potrebbe aver modificato le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="d3a1f-112">La finestra di dialogo Formato video è univoca per ogni driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="d3a1f-113">Alcuni driver di acquisizione potrebbero non supportare la finestra di dialogo Formato video.</span><span class="sxs-lookup"><span data-stu-id="d3a1f-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="d3a1f-114">Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoFormat** di [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span><span class="sxs-lookup"><span data-stu-id="d3a1f-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a1f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3a1f-115">Requirements</span></span>



| <span data-ttu-id="d3a1f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a1f-116">Requirement</span></span> | <span data-ttu-id="d3a1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d3a1f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d3a1f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a1f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a1f-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3a1f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d3a1f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a1f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a1f-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3a1f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3a1f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3a1f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a1f-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a1f-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a1f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3a1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a1f-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d3a1f-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d3a1f-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d3a1f-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





