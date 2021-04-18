---
title: Coordinate di trama generate automaticamente (Direct3D 9)
description: Il sistema può usare la posizione di spazio della fotocamera trasformata o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per indirizzare una mappa dell'ambiente cubica.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305113"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="02f4d-103">Coordinate di trama generate automaticamente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="02f4d-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="02f4d-104">Il sistema può usare la posizione di spazio della fotocamera trasformata o la normale da un vertice come coordinate di trama oppure può calcolare i tre vettori di elementi usati per indirizzare una mappa dell'ambiente cubica.</span><span class="sxs-lookup"><span data-stu-id="02f4d-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="02f4d-105">Analogamente alle coordinate di trama specificate in modo esplicito in un vertice, è possibile usare le coordinate di trama generate automaticamente come input per le trasformazioni di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="02f4d-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="02f4d-106">Le coordinate di trama generate automaticamente possono ridurre significativamente la larghezza di banda necessaria per i dati di geometria eliminando la necessità di coordinate di trama esplicite nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="02f4d-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="02f4d-107">In molti casi, le coordinate di trama generate dal sistema possono essere usate con le trasformazioni per produrre effetti speciali.</span><span class="sxs-lookup"><span data-stu-id="02f4d-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="02f4d-108">Naturalmente, si tratta di una funzionalità per scopi specifici e si useranno coordinate di trama esplicite per molte occasioni.</span><span class="sxs-lookup"><span data-stu-id="02f4d-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="02f4d-109">Configurazione delle coordinate di trama generate automaticamente</span><span class="sxs-lookup"><span data-stu-id="02f4d-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="02f4d-110">In C++ lo stato della \_ fase di trama D3DTSS TEXCOORDINDEX (dal tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) controlla il modo in cui il sistema genera le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="02f4d-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="02f4d-111">In genere, questo stato indica al sistema di usare un particolare set di coordinate di trama codificate in formato vertice.</span><span class="sxs-lookup"><span data-stu-id="02f4d-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="02f4d-112">Quando si includono i \_ flag D3DTSS TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION o D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR nel valore assegnato a questo stato, il comportamento del sistema è piuttosto diverso.</span><span class="sxs-lookup"><span data-stu-id="02f4d-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="02f4d-113">Se uno di questi flag è presente, la fase di trama ignora le coordinate di trama all'interno del formato del vertice a favore delle coordinate generate dal sistema.</span><span class="sxs-lookup"><span data-stu-id="02f4d-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="02f4d-114">I significati per ogni flag sono riportati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="02f4d-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="02f4d-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="02f4d-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="02f4d-116">Usare il vertice normale, trasformato nello spazio della fotocamera, come coordinate di trama di input.</span><span class="sxs-lookup"><span data-stu-id="02f4d-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="02f4d-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="02f4d-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="02f4d-118">Usare la posizione del vertice, trasformata nello spazio della fotocamera, come coordinate di trama di input.</span><span class="sxs-lookup"><span data-stu-id="02f4d-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="02f4d-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="02f4d-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="02f4d-120">Usare il vettore di reflection, trasformato nello spazio della fotocamera, come coordinate di trama di input.</span><span class="sxs-lookup"><span data-stu-id="02f4d-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="02f4d-121">Il vettore di reflection viene calcolato dalla posizione del vertice di input e dal vettore normale.</span><span class="sxs-lookup"><span data-stu-id="02f4d-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="02f4d-122">I flag di indice delle coordinate di trama si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="02f4d-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="02f4d-123">Questo esempio USA:</span><span class="sxs-lookup"><span data-stu-id="02f4d-123">This example uses:</span></span>

-   <span data-ttu-id="02f4d-124">Posizione del vertice (nello spazio della fotocamera) come coordinate di trama di input per questa fase della trama</span><span class="sxs-lookup"><span data-stu-id="02f4d-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="02f4d-125">Modalità a capo impostata nello stato di \_ rendering WRAP1 di D3DRENDERSTATE</span><span class="sxs-lookup"><span data-stu-id="02f4d-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="02f4d-126">Le coordinate di trama generate automaticamente sono più utili come valori di input per una trasformazione di coordinate di trama o per eliminare la necessità che l'applicazione calcoli i vettori di tre elementi per le mappe dell'ambiente cubico.</span><span class="sxs-lookup"><span data-stu-id="02f4d-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="02f4d-127">Il mapping di Sphere usa una mappa di trama pre-calcolata (al momento del modello) che contiene l'intero ambiente come riflesso da una sfera cromata.</span><span class="sxs-lookup"><span data-stu-id="02f4d-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="02f4d-128">Direct3D dispone di una funzionalità di generazione di coordinate di trama che usa lo stato di rendering D3DTSS \_ TCI \_ CAMERASPACENORMAL, che usa la normale parte del vertice nello spazio della fotocamera e la inserisce in una trasformazione di trama per generare coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="02f4d-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f4d-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02f4d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f4d-130">Elaborazione delle coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="02f4d-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="02f4d-131">Trasformazioni di coordinate di trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="02f4d-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="02f4d-132">Mapping dell'ambiente cubico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="02f4d-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
