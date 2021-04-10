---
description: Considerazioni sulle prestazioni (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considerazioni sulle prestazioni (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049135"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="749d4-103">Considerazioni sulle prestazioni (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="749d4-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="749d4-104">Uso di pool di effetti</span><span class="sxs-lookup"><span data-stu-id="749d4-104">Using Effect Pools</span></span>

<span data-ttu-id="749d4-105">Per il rendering di pipeline è comune usare molti shader per eseguire il rendering di tipi di oggetto e effetti speciali diversi.</span><span class="sxs-lookup"><span data-stu-id="749d4-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="749d4-106">Lo shader è costituito da una combinazione di stati comuni tra tutti gli shader, ad esempio una matrice globale o una posizione chiara e un altro stato specifico per ogni shader, ad esempio il colore diffuso di un oggetto o il calcolo dell'evidenziazione speculare.</span><span class="sxs-lookup"><span data-stu-id="749d4-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="749d4-107">Un pool di effetti è una posizione in memoria per archiviare lo stato utilizzato in molti shader, oltre a oggetti dispositivo comuni, ad esempio shader, oggetti di stato di rendering e buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="749d4-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="749d4-108">Il miglioramento delle prestazioni risulta dall'aggiornamento dello stato comune per tutti gli shader che necessitano di tale stato.</span><span class="sxs-lookup"><span data-stu-id="749d4-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="749d4-109">Un pool di effetti è una posizione di memoria condivisa per lo stato dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="749d4-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="749d4-110">Un pool viene creato in modo analogo a un effetto; è possibile crearla dalla memoria (oppure da un file o una risorsa).</span><span class="sxs-lookup"><span data-stu-id="749d4-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="749d4-111">Questo comporta due diversi tipi di effetti: un effetto globale che non dipende dallo stato in altro effetto rispetto a un effetto figlio che dipende dallo stato in un altro effetto.</span><span class="sxs-lookup"><span data-stu-id="749d4-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="749d4-112">Si specifica se un effetto è un effetto globale (caso predefinito) o un effetto figlio (specificando il flag dell' [effetto \_ \_ \_ \_ figlio compila effetto D3D10](d3d10-effect.md) ) quando viene creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="749d4-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="749d4-113">Un effetto globale può fungere da pool di effetti; un effetto figlio non può essere un pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="749d4-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="749d4-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="749d4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="749d4-115">Rendering di un effetto</span><span class="sxs-lookup"><span data-stu-id="749d4-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="749d4-116">Effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="749d4-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



