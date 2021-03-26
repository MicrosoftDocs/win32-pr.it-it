---
title: Direct3D 11 su hardware di livello inferiore
description: Questa sezione illustra il modo in cui Direct3D 11 è progettato per supportare hardware nuovi ed esistenti, da DirectX 9 a DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104557583"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="aacea-103">Direct3D 11 su hardware di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="aacea-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="aacea-104">Questa sezione illustra il modo in cui Direct3D 11 è progettato per supportare hardware nuovi ed esistenti, da DirectX 9 a DirectX 11.</span><span class="sxs-lookup"><span data-stu-id="aacea-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="aacea-105">Questo diagramma illustra in che modo Direct3D 11 supporta hardware nuovo ed esistente.</span><span class="sxs-lookup"><span data-stu-id="aacea-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![diagramma dell'hardware supportato da Direct3D 11](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="aacea-107">Con Direct3D 11, viene introdotto un nuovo paradigma denominato livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aacea-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="aacea-108">Un livello di funzionalità è un set di funzionalità GPU ben definito.</span><span class="sxs-lookup"><span data-stu-id="aacea-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="aacea-109">Utilizzando un livello di funzionalità, è possibile fare riferimento a un'applicazione Direct3D per l'esecuzione in una versione di livello inferiore di hardware Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aacea-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="aacea-110">Nella sezione di [riferimento 10Level9](d3d11-graphics-reference-10level9.md) sono elencate le differenze tra il comportamento di diversi metodi [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) a diversi livelli di funzionalità di 10Level9.</span><span class="sxs-lookup"><span data-stu-id="aacea-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="aacea-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="aacea-111">In this section</span></span>



| <span data-ttu-id="aacea-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="aacea-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="aacea-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aacea-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aacea-114">Livelli di funzionalità Direct3D</span><span class="sxs-lookup"><span data-stu-id="aacea-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="aacea-115">In questo argomento vengono illustrati i livelli di funzionalità Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aacea-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="aacea-116">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="aacea-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="aacea-117">Questo argomento descrive le eccezioni quando si usa Direct3D 11 su hardware di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="aacea-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="aacea-118">Compute Shaders su hardware di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="aacea-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="aacea-119">Questo argomento illustra come usare [Compute Shaders](direct3d-11-advanced-stages-compute-shader.md) in un'app Direct3D 11 su hardware Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="aacea-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="aacea-120">Prevenzione del SRVs di pixel shader NULL indesiderati</span><span class="sxs-lookup"><span data-stu-id="aacea-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="aacea-121">In questo argomento viene illustrato come aggirare il driver che riceve i **valori null** shader-Resource views (SRVs) anche quando SRVs non **null** sono associati alla fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="aacea-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="aacea-122">Procedure per i livelli di funzionalità</span><span class="sxs-lookup"><span data-stu-id="aacea-122">How to topics about feature levels</span></span>



| <span data-ttu-id="aacea-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="aacea-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="aacea-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aacea-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="aacea-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Procedura: ottenere il livello di funzionalità del dispositivo](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="aacea-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="aacea-126">Come ottenere un livello di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aacea-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="aacea-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aacea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aacea-128">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="aacea-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





