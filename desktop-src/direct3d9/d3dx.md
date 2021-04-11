---
description: D3DX è una raccolta di strumenti progettati per fornire funzionalità grafiche aggiuntive oltre a Direct3D. D3DX viene fornito come libreria a collegamento dinamico (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342211"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="c9d51-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9d51-104">D3DX (Direct3D 9)</span></span>

<span data-ttu-id="c9d51-105">D3DX è una raccolta di strumenti progettati per fornire funzionalità grafiche aggiuntive oltre a Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c9d51-105">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="c9d51-106">D3DX viene fornito come libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="c9d51-106">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="c9d51-107">In questa versione di DirectX SDK è disponibile una sola versione di D3DX.</span><span class="sxs-lookup"><span data-stu-id="c9d51-107">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="c9d51-108">La DLL D3DX per la vendita al dettaglio è inclusa nel pacchetto ridistribuibile fornito nell'SDK e viene installata automaticamente come parte dell' [installazione di DirectX con DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c9d51-108">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx).</span></span> <span data-ttu-id="c9d51-109">La libreria D3DX inclusa in questa versione dipende dai runtime Direct3D forniti con questo SDK.</span><span class="sxs-lookup"><span data-stu-id="c9d51-109">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="c9d51-110">Le applicazioni che si collegano alla versione di D3DX in questa versione devono anche ridistribuire il runtime da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="c9d51-110">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="c9d51-111">Più versioni di D3DX possono risiedere in modo indipendente in un singolo sistema simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="c9d51-111">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="c9d51-112">Collegando in modo statico un'applicazione a D3dx9. lib, l'applicazione si collega dinamicamente alla DLL D3DX Retail corrispondente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c9d51-112">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="c9d51-113">Questa DLL corrisponde alle intestazioni D3DX in base a cui viene compilata l'applicazione (denominata con la \_ \_ costante della versione SDK di D3DX in D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="c9d51-113">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="c9d51-114">Poiché le nuove versioni di D3DX vengono fornite nelle versioni future di DirectX SDK, le applicazioni che si collegano a librerie D3DX precedenti non saranno interessate.</span><span class="sxs-lookup"><span data-stu-id="c9d51-114">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="c9d51-115">La libreria D3DX risolve le seguenti aree generali di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="c9d51-115">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="c9d51-116">Supporto per disegno linee in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9d51-116">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="c9d51-117">Supporto mesh in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9d51-117">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="c9d51-118">Supporto della funzione Math in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9d51-118">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="c9d51-119">Supporto della trama in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9d51-119">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="c9d51-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9d51-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d51-121">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="c9d51-121">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



