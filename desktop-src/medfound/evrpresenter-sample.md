---
description: Esempio EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Esempio EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127890"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="bbae1-103">Esempio EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="bbae1-103">EVRPresenter Sample</span></span>

<span data-ttu-id="bbae1-104">Viene illustrato come implementare un presentatore personalizzato per il [renderer video avanzato](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="bbae1-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="bbae1-105">Il Presenter personalizzato può essere usato con il filtro EVR DirectShow o con il sink EVR Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="bbae1-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="bbae1-106">API illustrate</span><span class="sxs-lookup"><span data-stu-id="bbae1-106">APIs Demonstrated</span></span>

<span data-ttu-id="bbae1-107">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbae1-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="bbae1-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="bbae1-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="bbae1-109">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="bbae1-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="bbae1-110">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="bbae1-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="bbae1-111">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bbae1-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="bbae1-112">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="bbae1-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="bbae1-113">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="bbae1-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="bbae1-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bbae1-114">Usage</span></span>

<span data-ttu-id="bbae1-115">L'esempio EVRPresenter compila una DLL che è un server COM per il relatore.</span><span class="sxs-lookup"><span data-stu-id="bbae1-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="bbae1-116">Prima di utilizzare il Presenter personalizzato, è necessario registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="bbae1-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="bbae1-117">Per usare questo esempio in Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="bbae1-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="bbae1-118">Compilare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="bbae1-118">Build the sample.</span></span>
2.  <span data-ttu-id="bbae1-119">Regsvr32 EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="bbae1-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="bbae1-120">Compilare ed eseguire l' [esempio MFPlayer](/previous-versions//bb970516(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bbae1-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="bbae1-121">Scegliere **Apri** file dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="bbae1-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="bbae1-122">Nella finestra di dialogo **Apri file** selezionare **Custom EVR Presenter.**</span><span class="sxs-lookup"><span data-stu-id="bbae1-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="bbae1-123">Selezionare un file per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bbae1-123">Select a file for playback.</span></span>

<span data-ttu-id="bbae1-124">Per usare questo esempio in DirectShow:</span><span class="sxs-lookup"><span data-stu-id="bbae1-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="bbae1-125">Compilare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="bbae1-125">Build the sample.</span></span>
2.  <span data-ttu-id="bbae1-126">Registra EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="bbae1-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="bbae1-127">Compilare ed eseguire l'esempio EVRPlayer.</span><span class="sxs-lookup"><span data-stu-id="bbae1-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="bbae1-128">Questo esempio è incluso negli esempi di DirectShow nell'Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bbae1-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="bbae1-129">Scegliere **EVR Presenter** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="bbae1-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="bbae1-130">Selezionare un file per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bbae1-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbae1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbae1-131">Requirements</span></span>



| <span data-ttu-id="bbae1-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bbae1-132">Product</span></span>                                                        | <span data-ttu-id="bbae1-133">Versione</span><span class="sxs-lookup"><span data-stu-id="bbae1-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bbae1-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bbae1-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bbae1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbae1-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bbae1-136">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bbae1-136">Downloading the Sample</span></span>

<span data-ttu-id="bbae1-137">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="bbae1-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbae1-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbae1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbae1-139">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="bbae1-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="bbae1-140">Come scrivere un presentatore EVR</span><span class="sxs-lookup"><span data-stu-id="bbae1-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="bbae1-141">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="bbae1-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
