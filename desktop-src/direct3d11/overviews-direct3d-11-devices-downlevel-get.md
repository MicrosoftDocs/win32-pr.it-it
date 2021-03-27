---
title: Come ottenere il livello di funzionalità del dispositivo
description: In questo argomento viene illustrato come ottenere il livello di funzionalità massimo supportato da un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856701"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="37edc-103">Procedura: ottenere il livello di funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="37edc-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="37edc-104">In questo argomento viene illustrato come ottenere il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) massimo supportato da un [dispositivo](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="37edc-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="37edc-105">I dispositivi Direct3D 11 supportano un set fisso di livelli di funzionalità definiti nell'enumerazione [**del \_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="37edc-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="37edc-106">Quando si conosce il [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) più elevato supportato da un dispositivo, è possibile eseguire i percorsi del codice appropriati per tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37edc-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="37edc-107">**Per ottenere il livello di funzionalità del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="37edc-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="37edc-108">Chiamare la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o le funzioni [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) specificando **null** per il parametro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="37edc-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="37edc-109">Questa operazione può essere eseguita prima della creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37edc-109">You can do this before device creation.</span></span>

    <span data-ttu-id="37edc-110">\- - oppure -</span><span class="sxs-lookup"><span data-stu-id="37edc-110">\- or -</span></span>

    <span data-ttu-id="37edc-111">Chiamare [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) dopo la creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37edc-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="37edc-112">Esaminare il valore dell'enumerazione del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituito dall'ultimo passaggio per determinare il livello di funzionalità supportato.</span><span class="sxs-lookup"><span data-stu-id="37edc-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="37edc-113">Nell'esempio di codice seguente viene illustrato come determinare il livello di funzionalità massimo supportato chiamando la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) .</span><span class="sxs-lookup"><span data-stu-id="37edc-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="37edc-114">**D3D11CreateDevice** archivia il livello di funzionalità massimo supportato nella variabile FeatureLevel.</span><span class="sxs-lookup"><span data-stu-id="37edc-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="37edc-115">È possibile utilizzare questo codice per esaminare il valore del tipo enumerato del [**\_ \_ livello di funzionalità D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) restituito da **D3D11CreateDevice** .</span><span class="sxs-lookup"><span data-stu-id="37edc-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="37edc-116">Si noti che questo codice elenca tutti i livelli di funzionalità in modo esplicito (per Direct3D 11,1 e Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="37edc-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="37edc-117">Se il runtime Direct3D 11,1 è presente nel computer e *pFeatureLevels* è impostato su **null**, questa funzione non creerà un dispositivo [**D3D a \_ livello di funzionalità \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="37edc-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="37edc-118">Per creare un dispositivo **D3D a \_ livello di funzionalità \_ \_ 11 \_ 1** , è necessario specificare in modo esplicito una matrice a **\_ \_ livello di funzionalità D3D** che includa il **livello di \_ funzionalità D3D \_ \_ 11 \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="37edc-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="37edc-119">Se si specifica una matrice a **\_ \_ livello di funzionalità D3D** che contiene il **livello di \_ funzionalità D3D \_ \_ 11 \_ 1** in un computer in cui non è installato il runtime Direct3D 11,1, questa funzione non riesce immediatamente con E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="37edc-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="37edc-120">Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.</span><span class="sxs-lookup"><span data-stu-id="37edc-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37edc-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37edc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37edc-122">Direct3D 11 su hardware di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="37edc-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="37edc-123">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="37edc-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




