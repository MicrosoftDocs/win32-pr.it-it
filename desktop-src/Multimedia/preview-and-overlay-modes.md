---
title: Modalità anteprima e sovrapposizione
description: Modalità anteprima e sovrapposizione
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Messaggio WM_CAP_SET_PREVIEW
- capPreview (macro)
- Messaggio WM_CAP_SET_PREVIEWRATE
- capPreviewRate (macro)
- Messaggio WM_CAP_SET_SCALE
- capPreviewScale (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955357"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="96409-109">Modalità anteprima e sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="96409-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="96409-110">Un driver di acquisizione può implementare due metodi per la visualizzazione di un flusso video in entrata, ovvero la modalità anteprima e la modalità sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="96409-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="96409-111">Se un driver di acquisizione implementa entrambi i metodi, l'utente può scegliere il metodo da usare.</span><span class="sxs-lookup"><span data-stu-id="96409-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="96409-112">La modalità di anteprima trasferisce i frame digitalizzati dall'hardware di acquisizione alla memoria di sistema e quindi Visualizza i frame digitalizzati nella finestra di acquisizione usando le funzioni GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="96409-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="96409-113">Le applicazioni potrebbero ridurre la frequenza di anteprima quando la finestra padre perde lo stato attivo e aumentare la frequenza di anteprima quando la finestra padre ottiene lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="96409-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="96409-114">Questa azione migliora la velocità di risposta generale del sistema perché l'operazione di anteprima è a elevato utilizzo di processori.</span><span class="sxs-lookup"><span data-stu-id="96409-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="96409-115">Sono disponibili tre messaggi per controllare l'operazione di anteprima.</span><span class="sxs-lookup"><span data-stu-id="96409-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="96409-116">Usare il messaggio di [**Anteprima di WM \_ Cap \_ set \_**](wm-cap-set-preview.md) per abilitare o disabilitare la modalità di anteprima inviando (o la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96409-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="96409-117">Usare il [**messaggio \_ \_ \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (o la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) per impostare la frequenza di visualizzazione dei frame in modalità di anteprima</span><span class="sxs-lookup"><span data-stu-id="96409-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="96409-118">Per abilitare o disabilitare il ridimensionamento del video di anteprima, usare il messaggio [**WM \_ Cap \_ set \_ scale**](wm-cap-set-scale.md) (o la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ).</span><span class="sxs-lookup"><span data-stu-id="96409-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="96409-119">Quando l'anteprima e la scalabilità sono entrambe abilitate, il fotogramma video acquisito viene allungato alle dimensioni della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96409-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="96409-120">L'abilitazione della modalità di anteprima Disabilita automaticamente la modalità overlay.</span><span class="sxs-lookup"><span data-stu-id="96409-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="96409-121">La modalità sovrimpressione è una funzione hardware che consente di visualizzare il contenuto del buffer di acquisizione sul monitoraggio senza utilizzare risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="96409-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="96409-122">È possibile abilitare e disabilitare la modalità overlay inviando il messaggio di [**\_ \_ \_ sovrimpressione set di WM**](wm-cap-set-overlay.md) (o la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96409-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="96409-123">L'abilitazione della modalità sovrapposizione Disabilita automaticamente la modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="96409-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="96409-124">È anche possibile impostare la posizione di scorrimento del fotogramma video nell'area client della finestra di acquisizione per la modalità di anteprima o la modalità di sovrapposizione inviando il messaggio di [**scorrimento di WM \_ Cap \_ set \_**](wm-cap-set-scroll.md) (o la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="96409-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




