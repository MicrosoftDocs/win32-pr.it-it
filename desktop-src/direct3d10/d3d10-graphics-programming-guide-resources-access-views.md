---
description: In Direct3D 10 le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Visualizzazioni trama (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335585"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="bea50-103">Visualizzazioni trama (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bea50-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="bea50-104">In Direct3D 10 le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria.</span><span class="sxs-lookup"><span data-stu-id="bea50-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="bea50-105">Una visualizzazione consente a una determinata fase della pipeline di accedere solo [alle sottorisorse](d3d10-graphics-programming-guide-resources-types.md) necessarie, nella rappresentazione desiderata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bea50-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="bea50-106">Una visualizzazione supporta la nozione di risorsa senza tipo.</span><span class="sxs-lookup"><span data-stu-id="bea50-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="bea50-107">Una risorsa senza tipo è una risorsa creata con una dimensione specifica ma non con un tipo di dati specifico.</span><span class="sxs-lookup"><span data-stu-id="bea50-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="bea50-108">I dati vengono interpretati in modo dinamico quando sono associati alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea50-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="bea50-109">La figura seguente mostra un esempio di associazione di una matrice di trame 2D con 6 trame come risorsa shader creando una visualizzazione delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="bea50-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="bea50-110">La risorsa viene quindi indirizzata come matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="bea50-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="bea50-111">Nota: una sottorisorsa non può essere associata contemporaneamente come input e output alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea50-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![illustrazione di una matrice di trame con sei trame](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="bea50-113">Quando si usa una matrice di trame 2D come destinazione di rendering, la risorsa può essere visualizzata come matrice di trame 2D (6 in questo esempio) con livelli mipmap (3 in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="bea50-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="bea50-114">Creare un oggetto visualizzazione per una destinazione di rendering chiamando CreateRenderTargetView.</span><span class="sxs-lookup"><span data-stu-id="bea50-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="bea50-115">Chiamare quindi OMSetRenderTargets per impostare la visualizzazione della destinazione di rendering sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea50-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="bea50-116">Eseguire il rendering nelle destinazioni di rendering chiamando Draw e usando RenderTargetArrayIndex per indicizzare la trama appropriata nella matrice.</span><span class="sxs-lookup"><span data-stu-id="bea50-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="bea50-117">È possibile usare una sottorisorsa (una combinazione di livello mipmap e indice di matrice) per eseguire l'associazione a qualsiasi matrice di sottorisorse.</span><span class="sxs-lookup"><span data-stu-id="bea50-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="bea50-118">È quindi possibile eseguire l'associazione al secondo livello mipmap e aggiornare questo particolare livello di mipmap solo se si vuole, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="bea50-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![illustrazione del binding solo al secondo livello mipmap di una matrice di trame](images/d3d10-cube-texture-faces-subresource.png)



<span data-ttu-id="bea50-120">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="bea50-120">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="bea50-121">In Direct3D 10 non si associa più una risorsa direttamente alla pipeline, si crea una visualizzazione di una risorsa e quindi si imposta la visualizzazione sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea50-121">In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="bea50-122">In questo modo la convalida e il mapping nel runtime e nel driver possono verificarsi durante la creazione della visualizzazione, riducendo al minimo il controllo dei tipi in fase di associazione.</span><span class="sxs-lookup"><span data-stu-id="bea50-122">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="bea50-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bea50-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bea50-124">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="bea50-124">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




