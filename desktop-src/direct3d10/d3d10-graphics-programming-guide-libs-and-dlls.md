---
description: Per eseguire correttamente un'applicazione, è necessario che nel computer host siano installate le DLL appropriate. Queste dll possono essere fornite dal sistema operativo o dal pacchetto ridistribuibile delle applicazioni.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Collegamento di librerie statiche e dinamiche (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304716"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="e07cd-104">Collegamento di librerie statiche e dinamiche (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e07cd-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="e07cd-105">Per eseguire correttamente un'applicazione, è necessario che nel computer host siano installate le DLL appropriate.</span><span class="sxs-lookup"><span data-stu-id="e07cd-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="e07cd-106">Queste dll possono essere fornite dal sistema operativo o dal pacchetto ridistribuibile delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e07cd-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="e07cd-107">Librerie che caricano le DLL appropriate</span><span class="sxs-lookup"><span data-stu-id="e07cd-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="e07cd-108">Le librerie incluse in DirectX SDK caricherà automaticamente le DLL appropriate in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e07cd-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="e07cd-109">L'eccezione a questa regola è d3dx10. lib/d3dx10d. lib, che caricherà il d3dx10.dll fornito con la versione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="e07cd-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="e07cd-110">Se, ad esempio, l'SDK scaricato include d3dx10 \_33.dll e d3dx10 \_34.dll, la libreria (d3dx10. lib) fornita con tale SDK caricherà d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="e07cd-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="e07cd-111">Se successivamente viene installato un SDK successivo contenente d3dx10 \_ 35. lib, d3dx10. lib dell'SDK precedente caricherà comunque d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="e07cd-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="e07cd-112">D3dx10. lib dell'SDK più recente caricherà d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="e07cd-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="e07cd-113">Ridistribuzione di file binari</span><span class="sxs-lookup"><span data-stu-id="e07cd-113">Redistributing Binaries</span></span>

<span data-ttu-id="e07cd-114">È possibile ridistribuire solo d3dx10.dll e versioni successive dello stesso file.</span><span class="sxs-lookup"><span data-stu-id="e07cd-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="e07cd-115">Per ridistribuire il file, è necessario utilizzare la funzione **DirectXSetup** .</span><span class="sxs-lookup"><span data-stu-id="e07cd-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="e07cd-116">Per informazioni dettagliate sull'uso di questa funzione e sulla combinazione di un pacchetto ridistribuibile, vedere [installazione di DirectX con DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="e07cd-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="e07cd-117">Tutti gli altri file binari necessari sono inclusi in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e07cd-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="e07cd-118">Gli unici file binari che è possibile ridistribuire sono quelli presenti nella directory seguente.</span><span class="sxs-lookup"><span data-stu-id="e07cd-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="e07cd-119">La tabella seguente descrive i binari che gli sviluppatori devono conoscere.</span><span class="sxs-lookup"><span data-stu-id="e07cd-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="e07cd-120">File binari Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e07cd-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="e07cd-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e07cd-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07cd-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="e07cd-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="e07cd-123">Componenti D3DX10 per la vendita al dettaglio e di debug; i componenti per la vendita al dettaglio possono essere ridistribuiti nel file CAB REDIST.</span><span class="sxs-lookup"><span data-stu-id="e07cd-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e07cd-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="e07cd-124">d3d10ref.dll</span></span>           | <span data-ttu-id="e07cd-125">Rasterizzazione riferimenti.</span><span class="sxs-lookup"><span data-stu-id="e07cd-125">Reference Rasterizer.</span></span> <span data-ttu-id="e07cd-126">Fornisce l'implementazione del software della pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="e07cd-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="e07cd-127">Inclusa solo come parte del Windows SDK o di DirectX SDK legacy e non può essere ridistribuita.</span><span class="sxs-lookup"><span data-stu-id="e07cd-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="e07cd-128">L'rasterizzazione dei riferimenti è destinato solo al debug.</span><span class="sxs-lookup"><span data-stu-id="e07cd-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="e07cd-129">Il collegamento esplicito non è necessario. il tentativo di creare un dispositivo di riferimento (vedere [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) caricherà questa dll se è presente.</span><span class="sxs-lookup"><span data-stu-id="e07cd-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="e07cd-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="e07cd-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="e07cd-131">Serie di utilità SDK che fungono da livello tra le chiamate API e l'esecuzione del runtime, inclusi il [livello di debug](d3d10-graphics-programming-guide-api-features-layers.md) e il livello di commutazione a riferimento.</span><span class="sxs-lookup"><span data-stu-id="e07cd-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="e07cd-132">Il collegamento esplicito non è necessario. Se viene creato un dispositivo con il flag di livello appropriato, questa DLL viene caricata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e07cd-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="e07cd-133">Questo componente è progettato solo a scopo di sviluppo e debug.</span><span class="sxs-lookup"><span data-stu-id="e07cd-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="e07cd-134">Inclusa solo come parte del Windows SDK o di DirectX SDK legacy e non può essere ridistribuita.</span><span class="sxs-lookup"><span data-stu-id="e07cd-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e07cd-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e07cd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e07cd-136">Guida di programmazione per Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e07cd-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e07cd-137">Grafica Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e07cd-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



