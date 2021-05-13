---
title: Coordinate di trama generate automaticamente (Direct3D 9)
description: Il sistema può usare la posizione trasformata dello spazio della fotocamera o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elemento usati per affrontare una mappa cubica dell'ambiente.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843292"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="19375-103">Coordinate di trama generate automaticamente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19375-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="19375-104">Il sistema può usare la posizione trasformata dello spazio della fotocamera o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per affrontare una mappa cubica dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="19375-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="19375-105">Analogamente alle coordinate di trama specificate in modo esplicito in un vertice, è possibile usare le coordinate di trama generate automaticamente come input per le trasformazioni delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="19375-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="19375-106">Le coordinate di trama generate automaticamente possono ridurre significativamente la larghezza di banda necessaria per i dati geometrici eliminando la necessità di coordinate di trama esplicite nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="19375-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="19375-107">In molti casi, le coordinate di trama generate dal sistema possono essere usate con trasformazioni per produrre effetti speciali.</span><span class="sxs-lookup"><span data-stu-id="19375-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="19375-108">Naturalmente, si tratta di una funzionalità speciale e si useranno coordinate di trama esplicite per molte occasioni.</span><span class="sxs-lookup"><span data-stu-id="19375-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="19375-109">Configurazione delle coordinate di trama generate automaticamente</span><span class="sxs-lookup"><span data-stu-id="19375-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="19375-110">In C++ lo stato della trama D3DTSS \_ TEXCOORDINDEX (dal tipo enumerato [**D3DTEXTURESTAGESTATETYPE)**](./d3dtexturestagestatetype.md) controlla il modo in cui il sistema genera le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="19375-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="19375-111">In genere, questo stato indica al sistema di usare un particolare set di coordinate di trama codificate nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="19375-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="19375-112">Quando si includono i flag D3DTSS \_ TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION o D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR nel valore assegnato a questo stato, il comportamento del sistema è piuttosto diverso.</span><span class="sxs-lookup"><span data-stu-id="19375-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="19375-113">Se uno di questi flag è presente, la fase della trama ignora le coordinate della trama all'interno del formato vertice a favore delle coordinate generate dal sistema.</span><span class="sxs-lookup"><span data-stu-id="19375-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="19375-114">I significati per ogni flag sono indicati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="19375-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="19375-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="19375-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="19375-116">Usare la normale vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input.</span><span class="sxs-lookup"><span data-stu-id="19375-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="19375-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="19375-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="19375-118">Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate della trama di input.</span><span class="sxs-lookup"><span data-stu-id="19375-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="19375-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="19375-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="19375-120">Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinate della trama di input.</span><span class="sxs-lookup"><span data-stu-id="19375-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="19375-121">Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.</span><span class="sxs-lookup"><span data-stu-id="19375-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="19375-122">I flag dell'indice delle coordinate di trama si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="19375-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="19375-123">Questo esempio usa:</span><span class="sxs-lookup"><span data-stu-id="19375-123">This example uses:</span></span>

-   <span data-ttu-id="19375-124">Posizione del vertice (nello spazio della fotocamera) come coordinate della trama di input per questa fase della trama</span><span class="sxs-lookup"><span data-stu-id="19375-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="19375-125">Modalità di ritorno a capo impostata nello stato di rendering D3DRENDERSTATE \_ WRAP1</span><span class="sxs-lookup"><span data-stu-id="19375-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="19375-126">Le coordinate di trama generate automaticamente sono particolarmente utili come valori di input per una trasformazione delle coordinate di trama o per eliminare la necessità che l'applicazione calcoli vettori a tre elementi per le mappe dell'ambiente cubico.</span><span class="sxs-lookup"><span data-stu-id="19375-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="19375-127">Il mapping sphere usa una mappa di trama pre-ricalcolata (in fase di modello) che contiene l'intero ambiente come riflesso da una sfera cromata.</span><span class="sxs-lookup"><span data-stu-id="19375-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="19375-128">Direct3D ha una funzionalità di generazione delle coordinate di trama che usa lo stato di rendering D3DTSS \_ TCI CAMERASPACENORMAL, che accetta la normale del vertice nello spazio della fotocamera e la inserisce in una trasformazione di trama per generare le coordinate della \_ trama.</span><span class="sxs-lookup"><span data-stu-id="19375-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19375-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19375-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19375-130">Elaborazione delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="19375-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="19375-131">Trasformazioni delle coordinate di trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19375-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="19375-132">Mapping dell'ambiente cubico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="19375-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
