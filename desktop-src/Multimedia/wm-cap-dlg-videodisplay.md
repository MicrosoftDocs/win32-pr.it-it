---
title: Messaggio di WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: Il \_ \_ \_ messaggio VIDEODISPLAY di WM Cap DLG Visualizza una finestra di dialogo in cui l'utente può impostare o modificare l'output del video.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964188"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="21723-104">\_ \_ Messaggio VIDEODISPLAY WM Cap DLG \_</span><span class="sxs-lookup"><span data-stu-id="21723-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="21723-105">Il messaggio **VIDEODISPLAY di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può impostare o modificare l'output del video.</span><span class="sxs-lookup"><span data-stu-id="21723-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="21723-106">Questa finestra di dialogo può contenere controlli che interessano la tonalità, il contrasto e la luminosità dell'immagine visualizzata, nonché l'allineamento del colore della chiave.</span><span class="sxs-lookup"><span data-stu-id="21723-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="21723-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .</span><span class="sxs-lookup"><span data-stu-id="21723-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="21723-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21723-108">Return Value</span></span>

<span data-ttu-id="21723-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="21723-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="21723-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="21723-110">Remarks</span></span>

<span data-ttu-id="21723-111">I controlli in questa finestra di dialogo non influiscono sui dati video digitati; che interessano solo l'output o la rivisualizzazione del segnale video.</span><span class="sxs-lookup"><span data-stu-id="21723-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="21723-112">La finestra di dialogo visualizzazione video è univoca per ogni driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="21723-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="21723-113">Alcuni driver di acquisizione potrebbero non supportare una finestra di dialogo per la visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="21723-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="21723-114">Le applicazioni possono determinare se il driver di acquisizione supporta questo messaggio controllando il membro **fHasDlgVideoDisplay** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="21723-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="21723-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21723-115">Requirements</span></span>



| <span data-ttu-id="21723-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="21723-116">Requirement</span></span> | <span data-ttu-id="21723-117">Valore</span><span class="sxs-lookup"><span data-stu-id="21723-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21723-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21723-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21723-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21723-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="21723-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21723-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21723-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21723-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21723-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21723-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21723-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="21723-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21723-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21723-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21723-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="21723-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="21723-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="21723-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





