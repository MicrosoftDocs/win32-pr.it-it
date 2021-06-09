---
description: Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca e non sovrapposta di un segnale 2D (ad esempio una trama) in una mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso di UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826329"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="2a7ce-103">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2a7ce-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="2a7ce-104">UVAtlas è stato originariamente fornito nella libreria di utilità D3DX9, ora deprecata.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="2a7ce-105">La versione più recente è disponibile in [UV Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)</span><span class="sxs-lookup"><span data-stu-id="2a7ce-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="2a7ce-106">Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca e non sovrapposta di un segnale 2D (ad esempio una trama) in una mesh.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="2a7ce-107">Tali tecniche includono:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-107">Such techniques include:</span></span>

-   <span data-ttu-id="2a7ce-108">Mapping normale/spostamento</span><span class="sxs-lookup"><span data-stu-id="2a7ce-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="2a7ce-109">Simulazioni PRT dello spazio delle trame e mappe di luce</span><span class="sxs-lookup"><span data-stu-id="2a7ce-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="2a7ce-110">Disegno di superficie</span><span class="sxs-lookup"><span data-stu-id="2a7ce-110">Surface painting</span></span>
-   <span data-ttu-id="2a7ce-111">Illuminazione dello spazio trame</span><span class="sxs-lookup"><span data-stu-id="2a7ce-111">Texture-space lighting</span></span>

<span data-ttu-id="2a7ce-112">La generazione manuale di un mapping UV univoco è spesso dispendiosa in termini di tempo e noiosa; Ciò vale soprattutto quando la geometria di input è complessa ed è necessario un utilizzo efficiente/a bassa distorsione dello spazio della trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="2a7ce-113">La figura seguente mostra una mesh di esempio e l'at atlas di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Mostra una mesh di esempio e l'at atlas di trama corrispondente.](images/uvatlas1.jpg)

<span data-ttu-id="2a7ce-115">Questo esempio mostra una mesh (a sinistra) e la mappa normale dello spazio UV corrispondente (a destra).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="2a7ce-116">Si noti che l'atlas delle trame contiene diversi gruppi o cluster di dati. Ogni cluster è denominato grafico e nell'esempio precedente, displays contiene i dati normali per una parte della mesh.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="2a7ce-117">Le API UVAtlas D3DX generano automaticamente un at atlas ottimale non sovrapposto alle trame.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="2a7ce-118">Le API forniscono parametri di input che consentono di:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="2a7ce-119">Ridurre al minimo l'estensione, la distorsione e il sottocampionamento della trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="2a7ce-120">Ottimizzare la densità di creazione di un pacchetto dello spazio tra le trame per un uso efficiente della memoria.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="2a7ce-121">Fornire un campionamento uniforme nella rete, riducendo al minimo le discontinuità nella frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="2a7ce-122">Funzionamento di UVAtlas</span><span class="sxs-lookup"><span data-stu-id="2a7ce-122">How UVAtlas Works</span></span>

<span data-ttu-id="2a7ce-123">Le API UVAtlas (vedere Funzioni [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generano un at aterno di trama partizionando una superficie in grafici e impacchettondo i grafici in un aterno di trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="2a7ce-124">Usare [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) per eseguire questi passaggi separatamente. oppure usare [**D3DXUVAtlasCrea per**](d3dxuvatlascreate.md) partizionare, parametrizzare e creare un pacchetto in una singola chiamata.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="2a7ce-125">Partizionamento e parametrizzazione di una mesh</span><span class="sxs-lookup"><span data-stu-id="2a7ce-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="2a7ce-126">Uso di tensori delle metriche integrati per controllare la parametrizzazione</span><span class="sxs-lookup"><span data-stu-id="2a7ce-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="2a7ce-127">Uso dei dati di adizia per le crease specificate dall'utente</span><span class="sxs-lookup"><span data-stu-id="2a7ce-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="2a7ce-128">Creazione di un pacchetto di grafici in un Atlas</span><span class="sxs-lookup"><span data-stu-id="2a7ce-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="2a7ce-129">Partizionamento e parametrizzazione di una mesh</span><span class="sxs-lookup"><span data-stu-id="2a7ce-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="2a7ce-130">In primo luogo, la mesh viene partizionata in grafici, quindi ogni grafico viene parametrizzato nel proprio \[ spazio UV 0,1. \]</span><span class="sxs-lookup"><span data-stu-id="2a7ce-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="2a7ce-131">Un cilindro può essere parametrizzato da un grafico; Una sfera, d'altra parte, richiederà due grafici, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![illustrazione di una sfera partizionata in due grafici](images/uvatlas3.jpg)

<span data-ttu-id="2a7ce-133">Una mesh che può essere parametrizzata con un singolo grafico viene classificata come "omeomorfica in un disco", vale a dire che è possibile distribuire un disco all'infinito flessibile e all'infinito e coprire perfettamente la geometria.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="2a7ce-134">Questa estensione, detta omomorfismo, è una funzione bidirezionale; ciò significa che è possibile passare da una parametrizzazione all'altra senza perdere informazioni.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="2a7ce-135">Pochissime mesh reali possono essere parametrizzate in due dimensioni senza separare la mesh in cluster o grafici.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="2a7ce-136">La figura seguente mostra un'altra mesh di esempio e l'at atlas di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Mostra una mesh di esempio con forme diverse e l'at atlas di trama corrispondente.](images/uvatlas2.jpg)

<span data-ttu-id="2a7ce-138">Esistono due parametri che determinano il numero di grafici creati:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="2a7ce-139">Numero massimo di grafici consentiti per l'at atlas</span><span class="sxs-lookup"><span data-stu-id="2a7ce-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="2a7ce-140">Quantità massima di estensione consentita per ogni grafico</span><span class="sxs-lookup"><span data-stu-id="2a7ce-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="2a7ce-141">La quantità di estensione determinerà il numero di grafici generati e la qualità complessiva del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="2a7ce-142">L'estensione va da 0,0 (senza estensione) a 1,0 (qualsiasi quantità di estensione).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="2a7ce-143">D3DXUVAtlasCreate e D3DXUVAtlasPartition restituiscono l'estensione massima generata dall'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="2a7ce-144">La figura seguente mostra un'altra mesh di esempio e l'at atlas di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![illustrazione di una mesh di esempio e del relativo at atlas di trama corrispondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="2a7ce-146">Uso di tensori delle metriche integrati per controllare la parametrizzazione</span><span class="sxs-lookup"><span data-stu-id="2a7ce-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="2a7ce-147">La priorità dello spazio della trama può essere specificata in base al triangolo.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="2a7ce-148">I tensori delle metriche integrati possono essere forniti per controllare il modo in cui i triangoli vengono allungati nell'at atlas dello spazio trame risultante.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="2a7ce-149">Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo D3DX IMT.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="2a7ce-150">Un tensore delle metriche integrato (o IMT) è una matrice simmetrica 2x2 che descrive come viene allungato un triangolo nell'ateroso.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="2a7ce-151">Ogni IMT è definito da 3 float e li chiama (a,b,c).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="2a7ce-152">Possono essere disposti in una matrice simmetrica 2x2 simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="2a7ce-153">L'IMT può quindi essere usato per trovare la distanza tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="2a7ce-154">Dati due vettori v1 e v2, dove :</span><span class="sxs-lookup"><span data-stu-id="2a7ce-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="2a7ce-155">La distanza tra v1 e v2 può essere calcolata come:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="2a7ce-156">In altre parole, il vettore (s,t) potrebbe essere la grandezza dell'estensione in una direzione arbitraria nello spazio u-v.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="2a7ce-157">In questo caso, il vettore s è una direzione dal primo al secondo vertice e t è il prodotto incrociato della normale e di .</span><span class="sxs-lookup"><span data-stu-id="2a7ce-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="2a7ce-158">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-158">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="2a7ce-159">Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e grafica D3DXComputeIMTFromTexture. \_</span><span class="sxs-lookup"><span data-stu-id="2a7ce-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="2a7ce-160">Specificare direttamente i dati IMT se si vuole controllare la modalità di allocazione dello spazio trame ai singoli triangoli.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="2a7ce-161">In questo modo, allocare più area nell'at atlas ad aree importanti di una mesh, ad esempio il viso o il logo del logo di un logo del logo del logo di un personaggio o le aree di una scena vicino al percorso a piedi di un giocatore.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="2a7ce-162">Specificando gli IMT che sono multipli della matrice di identità, i triangoli risultanti verranno ridimensionati in modo uniforme nello spazio della trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="2a7ce-163">Ad esempio, data una mappa normale ad alta risoluzione, è possibile calcolare IMT per fornire più spazio di trama alle aree di segnale di frequenza più elevata nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="2a7ce-164">I triangoli "flat" (mappati alle aree costanti della mappa normale originale) riceveranno meno spazio trame.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="2a7ce-165">I triangoli che contengono una grande quantità di dettagli normali della mappa riceveranno un'area di trama maggiore nel risultato finale.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="2a7ce-166">È quindi possibile ricampionare la mappa normale in una trama più piccola, ma mantenere i dettagli, oppure è possibile ricalcolare la mappa normale con il mapping UV ottimale.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="2a7ce-167">Uso dei dati di adizia per le crease specificate dall'utente</span><span class="sxs-lookup"><span data-stu-id="2a7ce-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="2a7ce-168">Le informazioni sull'adicenza definite dall'utente possono essere fornite alla funzione di partizionamento per descrivere le creazioni predefinite nella mesh e quindi definire un limite del grafico tra i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="2a7ce-169">Si tratta di un modo semplice per il chiamante di specificare il proprio partizionamento del grafico come input nell'algoritmo, che perfeziona ulteriormente i grafici per portare l'estensione al di sotto del massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="2a7ce-170">Esempio</span><span class="sxs-lookup"><span data-stu-id="2a7ce-170">Example</span></span>

<span data-ttu-id="2a7ce-171">Questo esempio illustra come è possibile usare le API UVAtlas e DirectX Viewer (Dxviewer.exe) per trovare e correggere le discontinuità nel modello che possono influire notevolmente sulle dimensioni dell'at atlas della trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="2a7ce-172">È possibile ottenere Dxviewer.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="2a7ce-173">Dxviewer.exe è stato rimosso da DirectX SDK dopo la versione di agosto 2009, quindi per ottenerlo è necessario almeno l'SDK di DirectX di agosto 2009.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="2a7ce-174">Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="2a7ce-175">Si supponga di aver iniziato con un modello nel software preferito per la generazione di contenuti(in questo esempio viene utilizzato un modello di testa dwarf creato in Maya).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="2a7ce-176">Esportare il modello con trama in un file con estensione x e creare un at atlas di trama con D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="2a7ce-177">L'at atlas risultante per le trame sarà simile all'illustrazione seguente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-177">The resulting texture atlas would look something like the following illustration.</span></span>

![illustrazione di un at atlas per un modello nano](images/uvatlas5.jpg)

<span data-ttu-id="2a7ce-179">L'atlas ha 22 grafici e un'estensione massima di 0,994.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="2a7ce-180">Osservare ora il modello con trame per vedere quanto l'ateroso della trama è mappato alla geometria.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="2a7ce-181">A tale scopo, caricare il modello nello strumento visualizzatore:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="2a7ce-182">Aprire lo strumento visualizzatore da Utilità DirectX.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="2a7ce-183">Caricare il file con estensione x facendo clic sul pulsante Apri.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="2a7ce-184">Per abilitare l'opzione di visualizzazione crease, fare clic sul pulsante visualizza e selezionare Creases from popup (Crea da popup).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="2a7ce-185">La figura seguente mostra cosa dovrebbe essere visualizzato nello strumento visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-185">The following illustration shows what you should see in the viewer tool.</span></span>

![illustrazione di una mesh con trama nello strumento visualizzatore](images/uvatlas6c.jpg)

<span data-ttu-id="2a7ce-187">Ogni linea è una crease che è un bordo adiacente tra due grafici nell'at atlas della trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="2a7ce-188">Il numero di grafici generati dall'algoritmo è causato da lievi differenze, probabilmente a causa di discontinuità nelle normali.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="2a7ce-189">Queste piccole differenze possono essere ridotte mediante la welding dei dati, ad esempio forzando dati quasi uguali.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="2a7ce-190">Per weld the normals and the skinweights:To weld the normals and the skinweights:To weld the normals and the skinweights:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="2a7ce-191">Eseguire lo strumento DirectX Ops (dxops.exe) con la riga di comando seguente nella mesh (sostituendo "modelName.x" con il nome del modello):</span><span class="sxs-lookup"><span data-stu-id="2a7ce-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="2a7ce-192">In questo modo vengono confrontati i valori normali e i pesi della interfaccia e, dove il valore è minore di 2,01, i dati vengono resi uguali.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="2a7ce-193">Le illustrazioni seguenti mostrano un primo sguardo per vedere le scrissi prima dellalding (a sinistra) e le scrissi dopo lalding (a destra):</span><span class="sxs-lookup"><span data-stu-id="2a7ce-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![illustrazione delle creazioni prima dellalding](images/uvatlas6a.jpg)![illustrazione delle creazioni dopo lalding](images/uvatlas6b.jpg)

<span data-ttu-id="2a7ce-196">Figura 7: Rimozione di creases mediante la welding</span><span class="sxs-lookup"><span data-stu-id="2a7ce-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="2a7ce-197">In questo esempio la welding ha rimosso 86 vertici dalla mesh di input.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="2a7ce-198">Con un minor numero di sfasamenti nella mesh, è possibile rigenerare l'at atlas, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![illustrazione del nuovo atlas con le crease rimosse](images/uvatlas8.jpg)

<span data-ttu-id="2a7ce-200">L'atlas ha solo 7 grafici e un'estensione massima di circa 0,0776.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="2a7ce-201">Il nuovo at atlas ora si inserisce in una trama più piccola (circa il 30% in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="2a7ce-202">Creazione di un pacchetto di grafici in un Atlas</span><span class="sxs-lookup"><span data-stu-id="2a7ce-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="2a7ce-203">Dopo che una mesh è stata partizionata in grafici con parametri singoli, i grafici devono essere suddivisi in modo efficiente in un'unica mappa di trama.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="2a7ce-204">Questa operazione viene eseguita come secondo passaggio di D3DXUVAtlasCreate o può essere richiamata in modo esplicito chiamando D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="2a7ce-205">I grafici impacchettati sono separati da una larghezza di margine specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="2a7ce-206">La larghezza della barra è la quantità di separazione tra i grafici e consente l'interpolazione bilineare e il mapping mip per evitare il rendering degli artefatti ai limiti del grafico.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="2a7ce-207">D3DX offre un'interfaccia per il riempimento automatico di questi canali. Per altre informazioni, vedere [**ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)</span><span class="sxs-lookup"><span data-stu-id="2a7ce-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="2a7ce-208">Integrazione di UVAtlas nella pipeline</span><span class="sxs-lookup"><span data-stu-id="2a7ce-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="2a7ce-209">Oltre a essere richiamate dall'artista prima della trama, queste funzioni possono essere integrate in una pipeline grafica automatizzata.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="2a7ce-210">Ad esempio, una chiamata UVAtlas può essere eseguita automaticamente dopo l'aggiornamento di un asset, prima di eseguire una simulazione PRT o un normale passaggio di mapping.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="2a7ce-211">In questo modo si evita la necessità di ripristinare manualmente il mapping UV di un oggetto se la topologia della mesh è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="2a7ce-212">Vedere uv [Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) per un esempio di utilizzo delle funzioni UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a7ce-213">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a7ce-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a7ce-214">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="2a7ce-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
