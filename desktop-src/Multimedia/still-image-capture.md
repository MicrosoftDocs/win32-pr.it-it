---
title: Acquisizione di Still-Image
description: Acquisizione di Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Messaggio WM_CAP_GRAB_FRAME_NOSTOP
- Messaggio WM_CAP_GRAB_FRAME
- capGrabFrameNoStop (macro)
- capGrabFrame (macro)
- Messaggio WM_CAP_EDIT_COPY
- capEditCopy (macro)
- Messaggio WM_CAP_FILE_SAVEDIB
- capFileSaveDIB (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116785"
---
# <a name="still-image-capture"></a><span data-ttu-id="005ac-111">Acquisizione di Still-Image</span><span class="sxs-lookup"><span data-stu-id="005ac-111">Still-Image Capture</span></span>

<span data-ttu-id="005ac-112">Se si vuole acquisire un singolo fotogramma come immagine ancora, è possibile usare il messaggio di cattura del frame di acquisizione di [**WM \_ Cap \_ \_ \_**](wm-cap-grab-frame-nostop.md) o la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) o [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) per acquisire l'immagine digitalizzata in un [**buffer frame interno \_ \_ \_**](wm-cap-grab-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="005ac-112">If you want to capture a single frame as a still image, you can use the [**WM\_CAP\_GRAB\_FRAME\_NOSTOP**](wm-cap-grab-frame-nostop.md) or [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message (or the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) or [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro) to capture the digitized image in an internal frame buffer.</span></span> <span data-ttu-id="005ac-113">È possibile bloccare la visualizzazione sull'immagine acquisita usando WM \_ Cap \_ afferra \_ frame.</span><span class="sxs-lookup"><span data-stu-id="005ac-113">You can freeze the display on the captured image by using WM\_CAP\_GRAB\_FRAME.</span></span> <span data-ttu-id="005ac-114">In caso contrario, usare WM \_ Cap \_ Acquisisci \_ frame \_ NOSTOP.</span><span class="sxs-lookup"><span data-stu-id="005ac-114">Otherwise, use WM\_CAP\_GRAB\_FRAME\_NOSTOP.</span></span>

<span data-ttu-id="005ac-115">Una volta acquisita, è possibile copiare l'immagine per l'uso da parte di altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="005ac-115">Once captured, you can copy the image for use by other applications.</span></span> <span data-ttu-id="005ac-116">È possibile copiare un'immagine dal buffer dei frame negli appunti usando il messaggio di [**\_ copia della \_ modifica \_ di WM Cap**](wm-cap-edit-copy.md) (o la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ).</span><span class="sxs-lookup"><span data-stu-id="005ac-116">You can copy an image from the frame buffer to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="005ac-117">È anche possibile copiare l'immagine dal buffer del frame a una bitmap indipendente dal dispositivo (DIB) usando il messaggio [**\_ \_ \_ SAVEDIB**](wm-cap-file-savedib.md) (o la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).</span><span class="sxs-lookup"><span data-stu-id="005ac-117">You can also copy the image from the frame buffer to a device-independent bitmap (DIB) by using the [**WM\_CAP\_FILE\_SAVEDIB**](wm-cap-file-savedib.md) message (or the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro).</span></span>

<span data-ttu-id="005ac-118">L'applicazione può anche usare i due messaggi di acquisizione con frame singolo per modificare un frame di sequenza in base al frame oppure per creare una sequenza di fotogrammi fotografica di time-lapse.</span><span class="sxs-lookup"><span data-stu-id="005ac-118">Your application can also use the two single-frame capture messages to edit a sequence frame by frame, or to create a time-lapse photography sequence.</span></span>

 

 




