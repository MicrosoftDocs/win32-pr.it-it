---
title: Finestre di dialogo video
description: Finestre di dialogo video
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Messaggio WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource (macro)
- Messaggio WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat (macro)
- Messaggio WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay (macro)
- Messaggio WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297892"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="306ca-111">Finestre di dialogo video</span><span class="sxs-lookup"><span data-stu-id="306ca-111">Video Dialog Boxes</span></span>

<span data-ttu-id="306ca-112">Ogni driver di acquisizione può fornire fino a quattro finestre di dialogo per controllare gli aspetti del processo di acquisizione e digitalizzazione dei video e per definire gli attributi di compressione usati per ridurre le dimensioni dei dati video.</span><span class="sxs-lookup"><span data-stu-id="306ca-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="306ca-113">Il contenuto di queste finestre di dialogo viene definito dal driver di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="306ca-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="306ca-114">La finestra di dialogo origine video consente di controllare la selezione dei canali e dei parametri di input video che interessano l'immagine video che viene digitata nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="306ca-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="306ca-115">Questa finestra di dialogo enumera i tipi di segnali che connettono l'origine video alla scheda di acquisizione (in genere SVHS e input compositi) e fornisce controlli per modificare la tonalità, il contrasto o la saturazione.</span><span class="sxs-lookup"><span data-stu-id="306ca-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="306ca-116">Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOSOURCE di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videosource.md) (o la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).</span><span class="sxs-lookup"><span data-stu-id="306ca-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="306ca-117">La finestra di dialogo Formato video controlla la selezione delle dimensioni del fotogramma video digitalizzato e la profondità dell'immagine e le opzioni di compressione del video acquisito.</span><span class="sxs-lookup"><span data-stu-id="306ca-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="306ca-118">Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOFORMAT di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videoformat.md) (o la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).</span><span class="sxs-lookup"><span data-stu-id="306ca-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="306ca-119">La finestra di dialogo visualizzazione video consente di controllare l'aspetto del video nel monitoraggio durante l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="306ca-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="306ca-120">I controlli in questa finestra di dialogo non hanno alcun effetto sui dati video digitati, ma potrebbero influire sulla presentazione del segnale digitalizzato.</span><span class="sxs-lookup"><span data-stu-id="306ca-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="306ca-121">Ad esempio, i dispositivi di acquisizione che supportano la sovrapposizione possono consentire la modifica di tonalità, saturazione, colore della chiave o allineamento della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="306ca-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="306ca-122">Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEODISPLAY di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videodisplay.md) (o la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).</span><span class="sxs-lookup"><span data-stu-id="306ca-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="306ca-123">La finestra di dialogo compressione video controlla gli attributi di compressione video post-acquisizione.</span><span class="sxs-lookup"><span data-stu-id="306ca-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="306ca-124">Se la finestra di dialogo è supportata da un driver di acquisizione video, è possibile visualizzarla e aggiornarla usando il messaggio [**VIDEOCOMPRESSION di WM \_ Cap \_ DLG \_**](wm-cap-dlg-videocompression.md) (o la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).</span><span class="sxs-lookup"><span data-stu-id="306ca-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




