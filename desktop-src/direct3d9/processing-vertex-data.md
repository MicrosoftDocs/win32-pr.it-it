---
description: L'interfaccia IDirect3DDevice9 supporta l'elaborazione dei vertici in software e hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Elaborazione dei dati dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876818"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="63738-103">Elaborazione dei dati dei vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="63738-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="63738-104">L'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) supporta l'elaborazione dei vertici in software e hardware.</span><span class="sxs-lookup"><span data-stu-id="63738-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="63738-105">In generale, le funzionalità del dispositivo per l'elaborazione dei vertici hardware e software non sono identiche.</span><span class="sxs-lookup"><span data-stu-id="63738-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="63738-106">Le funzionalità hardware sono variabili, a seconda della scheda di visualizzazione e del driver, mentre le funzionalità software sono fisse.</span><span class="sxs-lookup"><span data-stu-id="63738-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="63738-107">I flag seguenti controllano il comportamento di elaborazione dei vertici per i dispositivi HAL (Hardware Abstraction Layer) e di riferimento.</span><span class="sxs-lookup"><span data-stu-id="63738-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="63738-108">D3DCREATE \_ software \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="63738-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="63738-109">\_VERTEXPROCESSING hardware \_ D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="63738-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="63738-110">D3DCREATE \_ misto \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="63738-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="63738-111">Specificare uno dei flag del comportamento di elaborazione dei vertici quando si chiama [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="63738-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="63738-112">Il flag in modalità mista consente al dispositivo di eseguire l'elaborazione dei vertici software e hardware.</span><span class="sxs-lookup"><span data-stu-id="63738-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="63738-113">È possibile impostare un solo flag di elaborazione dei vertici per un dispositivo in un momento qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="63738-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="63738-114">Si noti che \_ \_ è necessario impostare il flag VERTEXPROCESSING hardware D3DCREATE quando si crea un dispositivo puro (D3DCREATE \_ PUREDEVICE).</span><span class="sxs-lookup"><span data-stu-id="63738-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="63738-115">Per evitare funzionalità di elaborazione di due vertici su un solo dispositivo, è possibile eseguire query sulle funzionalità di elaborazione dei vertici hardware in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="63738-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="63738-116">Le funzionalità di elaborazione dei vertici software sono fisse e non è possibile eseguire query in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="63738-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="63738-117">Il membro VertexProcessingCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina le funzionalità di elaborazione dei vertici hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63738-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="63738-118">Per l'elaborazione di vertici software sono supportate le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="63738-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="63738-119">membro D3DVTXPCAPS \_ DIRECTIONALLIGHTS di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="63738-120">membro D3DVTXPCAPS \_ LOCALVIEWER di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="63738-121">membro D3DVTXPCAPS \_ MATERIALSOURCE7 di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="63738-122">membro D3DVTXPCAPS \_ POSITIONALLIGHTS di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="63738-123">membro D3DVTXPCAPS \_ TEXGEN di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="63738-124">\_membro di interpolazione D3DVTXPCAPS di [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="63738-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="63738-125">Nella tabella seguente sono inoltre elencati i valori impostati per i membri della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per un dispositivo in modalità di elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="63738-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="63738-126">Membro</span><span class="sxs-lookup"><span data-stu-id="63738-126">Member</span></span>                 | <span data-ttu-id="63738-127">Funzionalità di elaborazione dei vertici software</span><span class="sxs-lookup"><span data-stu-id="63738-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="63738-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="63738-128">MaxActiveLights</span></span>        | <span data-ttu-id="63738-129">Nessuna limitazione</span><span class="sxs-lookup"><span data-stu-id="63738-129">Unlimited</span></span>                               |
| <span data-ttu-id="63738-130">MaxUserClipPlanes</span><span class="sxs-lookup"><span data-stu-id="63738-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="63738-131">6</span><span class="sxs-lookup"><span data-stu-id="63738-131">6</span></span>                                       |
| <span data-ttu-id="63738-132">MaxVertexBlendMatrices</span><span class="sxs-lookup"><span data-stu-id="63738-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="63738-133">4</span><span class="sxs-lookup"><span data-stu-id="63738-133">4</span></span>                                       |
| <span data-ttu-id="63738-134">MaxStreams</span><span class="sxs-lookup"><span data-stu-id="63738-134">MaxStreams</span></span>             | <span data-ttu-id="63738-135">16</span><span class="sxs-lookup"><span data-stu-id="63738-135">16</span></span>                                      |
| <span data-ttu-id="63738-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="63738-136">MaxVertexIndex</span></span>         | <span data-ttu-id="63738-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="63738-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="63738-138">In generale, qualsiasi applicazione che è associata all'elaborazione dei vertici deve usare un dispositivo HAL.</span><span class="sxs-lookup"><span data-stu-id="63738-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="63738-139">L'elaborazione dei vertici software fornisce un set garantito di funzionalità di elaborazione vertici, tra cui un numero illimitato di luci e il supporto completo per i vertex shader programmabili.</span><span class="sxs-lookup"><span data-stu-id="63738-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="63738-140">Quando si usa il dispositivo HAL (che è l'unico tipo di dispositivo che supporta l'elaborazione dei vertici hardware e software), è possibile passare da un'elaborazione dei vertici software a un'altra in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="63738-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="63738-141">L'unico requisito è che i buffer vertex usati per l'elaborazione dei vertici software devono essere allocati nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="63738-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63738-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63738-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63738-143">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="63738-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
