---
description: Uso dei controlli schermo video
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Uso dei controlli schermo video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753826"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="94e26-103">Uso dei controlli schermo video</span><span class="sxs-lookup"><span data-stu-id="94e26-103">Using the Video Display Controls</span></span>

<span data-ttu-id="94e26-104">L'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controlla il modo in cui il renderer video avanzato (EVR) Visualizza il video all'interno di una finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="94e26-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="94e26-105">Questa interfaccia può essere utilizzata sia in DirectShow che in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="94e26-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="94e26-106">Internamente, i controlli schermo video sono forniti dal Presenter predefinito di EVR.</span><span class="sxs-lookup"><span data-stu-id="94e26-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="94e26-107">Se si scrive un presentatore personalizzato, è possibile specificare la stessa interfaccia o definire un'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="94e26-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="94e26-108">Il modo corretto per ottenere un puntatore all'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) varia a seconda che si usi la versione DIRECTSHOW di EVR o la versione Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="94e26-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="94e26-109">Per il Media Foundation EVR, dipende anche dal fatto che il EVR venga usato direttamente o usato attraverso la sessione multimediale, che è più comune.</span><span class="sxs-lookup"><span data-stu-id="94e26-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="94e26-110">Per ottenere un puntatore all'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="94e26-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="94e26-111">Ottenere un puntatore all'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="94e26-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="94e26-112">Se si usa il filtro EVR DirectShow, chiamare **QueryInterface** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="94e26-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="94e26-113">Se si usa direttamente il sink di supporto EVR, chiamare **QueryInterface** sul sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="94e26-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="94e26-114">Se si usa la sessione multimediale, chiamare **QueryInterface** nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="94e26-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="94e26-115">Se si usa la sessione multimediale, attendere che la sessione multimediale invii l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con un valore di stato MF \_ TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="94e26-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="94e26-116">Ignorare questo passaggio in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="94e26-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="94e26-117">Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="94e26-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="94e26-118">L'identificatore del servizio è \_ il \_ servizio di rendering video \_ .</span><span class="sxs-lookup"><span data-stu-id="94e26-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="94e26-119">È possibile utilizzare l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="94e26-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="94e26-120">Impostare la finestra di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="94e26-120">Set the clipping window.</span></span>

-   <span data-ttu-id="94e26-121">Impostare i rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="94e26-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="94e26-122">Aggiornare la finestra video in risposta ai messaggi della finestra.</span><span class="sxs-lookup"><span data-stu-id="94e26-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="94e26-123">Abilitare o disabilitare la modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="94e26-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="94e26-124">Finestra di ritaglio</span><span class="sxs-lookup"><span data-stu-id="94e26-124">Clipping Window</span></span>

<span data-ttu-id="94e26-125">L'applicazione deve fornire una finestra in cui EVR disegna il video.</span><span class="sxs-lookup"><span data-stu-id="94e26-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="94e26-126">Per impostare la finestra di ridimensionamento, chiamare [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) con un handle per la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="94e26-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="94e26-127">Se si crea il sink del supporto EVR tramite il relativo oggetto Activation, questo passaggio non è necessario.</span><span class="sxs-lookup"><span data-stu-id="94e26-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="94e26-128">L'oggetto Activation chiama automaticamente [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), usando l'handle della finestra fornito nella funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="94e26-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="94e26-129">Rettangoli di origine e di destinazione</span><span class="sxs-lookup"><span data-stu-id="94e26-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="94e26-130">Durante la riproduzione, il Presenter acquisisce una parte dell'immagine video composita e la disegna su un'area della finestra video.</span><span class="sxs-lookup"><span data-stu-id="94e26-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="94e26-131">La parte dell'immagine composita è il *rettangolo di origine* e l'area della finestra video è il rettangolo di *destinazione*.</span><span class="sxs-lookup"><span data-stu-id="94e26-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="94e26-132">Il rettangolo di origine viene definito usando le coordinate normalizzate in cui il punto (0,0, 0,0) corrisponde all'angolo superiore sinistro del video e (1,0, 1,0) corrisponde all'angolo inferiore destro del video.</span><span class="sxs-lookup"><span data-stu-id="94e26-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="94e26-133">Il rettangolo di origine può essere qualsiasi area all'interno di questo rettangolo.</span><span class="sxs-lookup"><span data-stu-id="94e26-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="94e26-134">Il rettangolo di destinazione viene specificato in pixel rispetto all'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="94e26-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="94e26-135">Il rettangolo di origine predefinito è l'intera immagine e il rettangolo di destinazione predefinito è un rettangolo vuoto.</span><span class="sxs-lookup"><span data-stu-id="94e26-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="94e26-136">Per impostare i rettangoli di origine e di destinazione, chiamare [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="94e26-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="94e26-137">Se si crea il sink del supporto EVR tramite il relativo oggetto Activation, questo passaggio non è necessario.</span><span class="sxs-lookup"><span data-stu-id="94e26-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="94e26-138">L'oggetto Activation imposta automaticamente il rettangolo di destinazione uguale all'intera area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="94e26-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="94e26-139">Tuttavia, è necessario chiamare [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) se si desidera modificare il rettangolo di origine o impostare un rettangolo di destinazione diverso.</span><span class="sxs-lookup"><span data-stu-id="94e26-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="94e26-140">Messaggi finestra</span><span class="sxs-lookup"><span data-stu-id="94e26-140">Window Messages</span></span>

<span data-ttu-id="94e26-141">Durante la riproduzione, l'applicazione deve rispondere a determinati messaggi della finestra, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="94e26-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="94e26-142">\_Disegno WM: chiamare [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) per ridisegnare il video.</span><span class="sxs-lookup"><span data-stu-id="94e26-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="94e26-143">Evitare inoltre di disegnare sul rettangolo di destinazione durante la riproduzione del video, perché ciò può causare lo sfarfallio.</span><span class="sxs-lookup"><span data-stu-id="94e26-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="94e26-144">\_Dimensioni WM: potrebbe essere necessario chiamare [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) per ridimensionare il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="94e26-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="94e26-145">Diversamente dal filtro VMR (video Mixing Renderer) in DirectShow, non è necessario inviare una notifica al EVR quando si riceve un messaggio WM \_ DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="94e26-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94e26-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94e26-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94e26-147">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="94e26-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



