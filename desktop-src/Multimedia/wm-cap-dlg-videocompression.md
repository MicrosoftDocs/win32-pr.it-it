---
title: Messaggio di WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: Il \_ messaggio VIDEOCOMPRESSION di WM Cap \_ DLG \_ Visualizza una finestra di dialogo in cui l'utente può selezionare un compressore da usare durante il processo di acquisizione.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048333"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="09773-104">\_ \_ Messaggio VIDEOCOMPRESSION WM Cap DLG \_</span><span class="sxs-lookup"><span data-stu-id="09773-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="09773-105">Il messaggio **VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_** Visualizza una finestra di dialogo in cui l'utente può selezionare un compressore da usare durante il processo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="09773-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="09773-106">L'elenco dei commutatori disponibili può variare a seconda del formato video selezionato nella finestra di dialogo Formato video del driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="09773-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="09773-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="09773-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="09773-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09773-108">Return Value</span></span>

<span data-ttu-id="09773-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="09773-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09773-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="09773-110">Remarks</span></span>

<span data-ttu-id="09773-111">Utilizzare questo messaggio con i driver di acquisizione che forniscono frame solo nel \_ formato RGB bi.</span><span class="sxs-lookup"><span data-stu-id="09773-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="09773-112">Questo messaggio è particolarmente utile nell'operazione di acquisizione step per combinare l'acquisizione e la compressione in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="09773-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="09773-113">La compressione dei frame con un commediatore software come parte di un'operazione di acquisizione in tempo reale è molto probabilmente troppo dispendiosa in termini di tempo.</span><span class="sxs-lookup"><span data-stu-id="09773-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="09773-114">La compressione non influisce sui frame copiati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="09773-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="09773-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09773-115">Requirements</span></span>



| <span data-ttu-id="09773-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09773-116">Requirement</span></span> | <span data-ttu-id="09773-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09773-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="09773-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09773-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09773-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09773-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="09773-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09773-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09773-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09773-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="09773-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09773-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09773-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="09773-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09773-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09773-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09773-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="09773-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="09773-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="09773-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





