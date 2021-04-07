---
description: Questo argomento descrive il modo in cui un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurare la qualità del video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746055"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="fc776-103">Configurare la qualità del video</span><span class="sxs-lookup"><span data-stu-id="fc776-103">Configure the Video Quality</span></span>

<span data-ttu-id="fc776-104">Questo argomento descrive il modo in cui un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="fc776-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="fc776-105">Impostazioni ProcAmp</span><span class="sxs-lookup"><span data-stu-id="fc776-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="fc776-106">Impostazioni videocamera</span><span class="sxs-lookup"><span data-stu-id="fc776-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="fc776-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc776-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="fc776-108">Impostazioni ProcAmp</span><span class="sxs-lookup"><span data-stu-id="fc776-108">ProcAmp Settings</span></span>

<span data-ttu-id="fc776-109">Le videocamere Windows Driver Model (WDM) possono supportare le proprietà che controllano la qualità dell'immagine:</span><span class="sxs-lookup"><span data-stu-id="fc776-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="fc776-110">Compensazione retroilluminazione</span><span class="sxs-lookup"><span data-stu-id="fc776-110">Backlight compensation</span></span>
-   <span data-ttu-id="fc776-111">Luminosità</span><span class="sxs-lookup"><span data-stu-id="fc776-111">Brightness</span></span>
-   <span data-ttu-id="fc776-112">Si confronti</span><span class="sxs-lookup"><span data-stu-id="fc776-112">Contrast</span></span>
-   <span data-ttu-id="fc776-113">Ottenere</span><span class="sxs-lookup"><span data-stu-id="fc776-113">Gain</span></span>
-   <span data-ttu-id="fc776-114">Gamma</span><span class="sxs-lookup"><span data-stu-id="fc776-114">Gamma</span></span>
-   <span data-ttu-id="fc776-115">Tonalità</span><span class="sxs-lookup"><span data-stu-id="fc776-115">Hue</span></span>
-   <span data-ttu-id="fc776-116">Saturazione</span><span class="sxs-lookup"><span data-stu-id="fc776-116">Saturation</span></span>
-   <span data-ttu-id="fc776-117">Nitidezza</span><span class="sxs-lookup"><span data-stu-id="fc776-117">Sharpness</span></span>
-   <span data-ttu-id="fc776-118">Bilanciamento del bianco</span><span class="sxs-lookup"><span data-stu-id="fc776-118">White balance</span></span>

<span data-ttu-id="fc776-119">Queste proprietà vengono controllate tramite l'interfaccia [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="fc776-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="fc776-120">Usare questa interfaccia come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="fc776-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="fc776-121">Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul filtro di acquisizione per l'interfaccia [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="fc776-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="fc776-122">Per ogni proprietà che si desidera impostare, chiamare il metodo [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) .</span><span class="sxs-lookup"><span data-stu-id="fc776-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="fc776-123">Le proprietà vengono specificate dall'enumerazione [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) .</span><span class="sxs-lookup"><span data-stu-id="fc776-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="fc776-124">Se il metodo **GetRange** ha esito negativo, significa che la fotocamera non supporta la proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="fc776-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="fc776-125">Se [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) ha esito positivo, restituisce l'intervallo di valori supportati per la proprietà, il valore predefinito e l'incremento minimo.</span><span class="sxs-lookup"><span data-stu-id="fc776-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="fc776-126">Per ottenere il valore corrente di una proprietà, chiamare [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="fc776-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="fc776-127">Per impostare una proprietà, chiamare il metodo [**IAMVideoProcAmp:: set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) .</span><span class="sxs-lookup"><span data-stu-id="fc776-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="fc776-128">Per ripristinare il valore predefinito di una proprietà, chiamare [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) per individuare il valore predefinito e passare tale valore al metodo **set** .</span><span class="sxs-lookup"><span data-stu-id="fc776-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="fc776-129">Non è necessario arrestare il grafico dei filtri quando si impostano le proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc776-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="fc776-130">Il codice seguente configura un controllo TrackBar in modo che possa essere usato per impostare la luminosità.</span><span class="sxs-lookup"><span data-stu-id="fc776-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="fc776-131">L'intervallo del TrackBar corrisponde all'intervallo di luminosità supportato dal dispositivo e la posizione del TrackBar corrisponde all'impostazione della luminosità iniziale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc776-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="fc776-132">Impostazioni videocamera</span><span class="sxs-lookup"><span data-stu-id="fc776-132">Camera Settings</span></span>

<span data-ttu-id="fc776-133">L'interfaccia [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) è simile a [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), ma controlla diversi setttings nella fotocamera:</span><span class="sxs-lookup"><span data-stu-id="fc776-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="fc776-134">Esposizione</span><span class="sxs-lookup"><span data-stu-id="fc776-134">Exposure</span></span>
-   <span data-ttu-id="fc776-135">Focus</span><span class="sxs-lookup"><span data-stu-id="fc776-135">Focus</span></span>
-   <span data-ttu-id="fc776-136">Iris</span><span class="sxs-lookup"><span data-stu-id="fc776-136">Iris</span></span>
-   <span data-ttu-id="fc776-137">Dettaglio</span><span class="sxs-lookup"><span data-stu-id="fc776-137">Pan</span></span>
-   <span data-ttu-id="fc776-138">Eseguire il rollback</span><span class="sxs-lookup"><span data-stu-id="fc776-138">Roll</span></span>
-   <span data-ttu-id="fc776-139">Inclinazione</span><span class="sxs-lookup"><span data-stu-id="fc776-139">Tilt</span></span>
-   <span data-ttu-id="fc776-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="fc776-140">Zoom</span></span>

<span data-ttu-id="fc776-141">Per usare questa interfaccia, seguire la stessa procedura usata per [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span><span class="sxs-lookup"><span data-stu-id="fc776-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="fc776-142">Eseguire una query sul filtro di acquisizione per [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span><span class="sxs-lookup"><span data-stu-id="fc776-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="fc776-143">Chiamare [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) per individuare le impostazioni supportate e il possibile intervallo per ogni impostazione.</span><span class="sxs-lookup"><span data-stu-id="fc776-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="fc776-144">Chiamare [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) per ottenere il valore corrente di un'impostazione.</span><span class="sxs-lookup"><span data-stu-id="fc776-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="fc776-145">Chiamare [**IAMCameraControl:: set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) per impostare il valore.</span><span class="sxs-lookup"><span data-stu-id="fc776-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc776-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc776-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc776-147">Configurazione di un dispositivo di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="fc776-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
