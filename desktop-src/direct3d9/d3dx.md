---
description: D3DX è una libreria di strumenti progettati per fornire funzionalità grafiche aggiuntive su Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910243"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="7efeb-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7efeb-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="7efeb-105">La libreria D3DX è deprecata.</span><span class="sxs-lookup"><span data-stu-id="7efeb-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="7efeb-106">Se l'aggiornamento a una versione più recente di Direct3D e al codice di utilità associato non è un'opzione, è possibile usare il pacchetto NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) invece di basarsi su DirectX SDK o DirectSetup legacy.</span><span class="sxs-lookup"><span data-stu-id="7efeb-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="7efeb-107">D3DX è una libreria di strumenti progettati per fornire funzionalità grafiche aggiuntive su Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7efeb-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="7efeb-108">D3DX viene fornito come libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="7efeb-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="7efeb-109">In questa versione di DirectX SDK è disponibile una sola versione di D3DX.</span><span class="sxs-lookup"><span data-stu-id="7efeb-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="7efeb-110">La DLL D3DX definitiva è inclusa nel file ridistribuibile fornito nell'SDK e viene installata automaticamente come parte dell'installazione di **DirectX con DirectSetup.**</span><span class="sxs-lookup"><span data-stu-id="7efeb-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="7efeb-111">La libreria D3DX inclusa in questa versione dipende dai runtime Direct3D forniti con questo SDK.</span><span class="sxs-lookup"><span data-stu-id="7efeb-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="7efeb-112">Anche le applicazioni che si collegano alla versione di D3DX in questa versione devono ridistribuire il runtime da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="7efeb-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="7efeb-113">Più versioni di D3DX possono risiedere in modo indipendente in un singolo sistema contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="7efeb-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="7efeb-114">Collegando in modo statico un'applicazione a D3dx9.lib, l'applicazione si collega in modo dinamico alla DLL D3DX finale corrispondente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7efeb-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="7efeb-115">Questa DLL corrisponde alle intestazioni D3DX con cui viene compilata l'applicazione (denominata con la costante VERSION di D3DX \_ SDK \_ in D3dx9core.h).</span><span class="sxs-lookup"><span data-stu-id="7efeb-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="7efeb-116">Poiché le nuove versioni di D3DX verranno rilasciate nelle versioni future di DirectX SDK, le applicazioni che si collegano alle librerie D3DX precedenti rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="7efeb-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="7efeb-117">La libreria D3DX risolve queste aree generali di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="7efeb-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="7efeb-118">Supporto per il disegno di linee in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7efeb-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="7efeb-119">Supporto mesh in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7efeb-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="7efeb-120">Supporto delle funzioni matematiche in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7efeb-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="7efeb-121">Supporto delle trame in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7efeb-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="7efeb-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7efeb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7efeb-123">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="7efeb-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



