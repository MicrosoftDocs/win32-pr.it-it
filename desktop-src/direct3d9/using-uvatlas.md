---
description: Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca non sovrapposta di un segnale 2D, ad esempio una trama, su una rete mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso di UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234407"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="1f7b0-103">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1f7b0-103">Using UVAtlas (Direct3D 9)</span></span>

<span data-ttu-id="1f7b0-104">Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca non sovrapposta di un segnale 2D, ad esempio una trama, su una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-104">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="1f7b0-105">Tali tecniche includono:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-105">Such techniques include:</span></span>

-   <span data-ttu-id="1f7b0-106">Mapping normale/spostamento</span><span class="sxs-lookup"><span data-stu-id="1f7b0-106">Normal/displacement mapping</span></span>
-   <span data-ttu-id="1f7b0-107">Texture-simulazioni PRT di spazio e mappe chiare</span><span class="sxs-lookup"><span data-stu-id="1f7b0-107">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="1f7b0-108">Disegno della superficie</span><span class="sxs-lookup"><span data-stu-id="1f7b0-108">Surface painting</span></span>
-   <span data-ttu-id="1f7b0-109">Illuminazione dello spazio di trama</span><span class="sxs-lookup"><span data-stu-id="1f7b0-109">Texture-space lighting</span></span>

<span data-ttu-id="1f7b0-110">La generazione manuale di un mapping UV univoco è spesso noiosa e dispendiosa in termini di tempo. Ciò è particolarmente vero quando la geometria di input è complessa ed efficiente/a bassa distorsione. si desidera utilizzare lo spazio.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-110">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="1f7b0-111">La figura seguente mostra una mesh di esempio e il relativo Atlante di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-111">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Mostra una mesh di esempio e il relativo Atlante di trama corrispondente.](images/uvatlas1.jpg)

<span data-ttu-id="1f7b0-113">Questo esempio mostra una mesh (a sinistra) e la mappa normale dello spazio UV corrispondente (sulla destra).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-113">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="1f7b0-114">Si noti che l'Atlante di trama contiene diversi gruppi o cluster di dati; ogni cluster è denominato grafico e nell'esempio precedente, Visualizza contiene i dati normali per una parte della mesh.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-114">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="1f7b0-115">Le API UVAtlas di D3DX generano automaticamente un Atlante di trama ottimale non sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-115">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="1f7b0-116">Le API forniscono parametri di input che consentono di:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-116">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="1f7b0-117">Ridurre al minimo l'estensione della trama, la distorsione e il sottocampionamento.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-117">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="1f7b0-118">Massimizza la densità di compressione dello spazio di trama per un uso efficiente della memoria.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-118">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="1f7b0-119">Fornire un campionamento uniforme sulla rete, riducendo al minimo le discontinuità nella frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-119">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="1f7b0-120">Funzionamento di UVAtlas</span><span class="sxs-lookup"><span data-stu-id="1f7b0-120">How UVAtlas Works</span></span>

<span data-ttu-id="1f7b0-121">Le API UVAtlas (vedere [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generano un Atlante di trama partizionando una superficie nei grafici e imballando i grafici in un Atlante di trama.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-121">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="1f7b0-122">Usare [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) per eseguire questi passaggi separatamente. in alternativa, usare [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) per partizionare, parametrizzare e comprimere in un'unica chiamata.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-122">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="1f7b0-123">Partizionamento e parametrizzazione di una mesh</span><span class="sxs-lookup"><span data-stu-id="1f7b0-123">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="1f7b0-124">Uso di tensori metrici integrati per controllare la parametrizzazione</span><span class="sxs-lookup"><span data-stu-id="1f7b0-124">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="1f7b0-125">Utilizzo di dati adiacenza per le pieghe specificate dall'utente</span><span class="sxs-lookup"><span data-stu-id="1f7b0-125">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="1f7b0-126">Compressione dei grafici in un Atlante</span><span class="sxs-lookup"><span data-stu-id="1f7b0-126">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="1f7b0-127">Partizionamento e parametrizzazione di una mesh</span><span class="sxs-lookup"><span data-stu-id="1f7b0-127">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="1f7b0-128">In primo luogo, la mesh viene partizionata in grafici, quindi ogni grafico viene sottoposto a parametrizzazione in un proprio \[ \] spazio UV di 0, 1.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-128">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="1f7b0-129">Un cilindro può essere parametrizzato da un grafico; una sfera è invece necessaria per due grafici, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-129">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![illustrazione di una sfera partizionata in due grafici](images/uvatlas3.jpg)

<span data-ttu-id="1f7b0-131">Una mesh che può essere parametrizzata con un singolo grafico è classificata come "omeomorfo su un disco", vale a dire che è possibile distribuire un disco infinitamente flessibile e infinitamente estensibile sul grafico e coprire la geometria perfettamente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-131">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="1f7b0-132">Questa estensione, denominata omeomorfismo, è una funzione bidirezionale. Ciò significa che è possibile passare da una parametrizzazione all'altra senza perdere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-132">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="1f7b0-133">Pochissime mesh reali possono essere parametrizzate in due dimensioni senza separare la mesh in cluster o grafici.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-133">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="1f7b0-134">La figura seguente mostra un altro mesh di esempio e il relativo Atlante di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-134">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Mostra un esempio di mesh con forme diverse e il relativo Atlante di trama corrispondente.](images/uvatlas2.jpg)

<span data-ttu-id="1f7b0-136">Sono disponibili due parametri che determinano il numero di grafici creati:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-136">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="1f7b0-137">Numero massimo di grafici consentiti per l'Atlante</span><span class="sxs-lookup"><span data-stu-id="1f7b0-137">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="1f7b0-138">Quantità massima di estensione consentita per ogni grafico</span><span class="sxs-lookup"><span data-stu-id="1f7b0-138">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="1f7b0-139">La quantità di estensione determinerà il numero di grafici generati e la qualità complessiva del campionamento.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-139">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="1f7b0-140">L'estensione varia da 0,0 (nessun tratto) a 1,0 (qualsiasi quantità di estensione).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-140">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="1f7b0-141">D3DXUVAtlasCreate e D3DXUVAtlasPartition restituiscono l'estensione massima generata dall'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-141">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="1f7b0-142">La figura seguente mostra un altro mesh di esempio e il relativo Atlante di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-142">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![illustrazione di una mesh di esempio e dell'Atlante di trama corrispondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="1f7b0-144">Uso di tensori metrici integrati per controllare la parametrizzazione</span><span class="sxs-lookup"><span data-stu-id="1f7b0-144">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="1f7b0-145">La definizione delle priorità dello spazio di trama può essere specificata in base ai singoli triangoli.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-145">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="1f7b0-146">È possibile fornire i tensori di metrica integrati per controllare il modo in cui i triangoli vengono estesi nell'Atlante di spazio di trama risultante.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-146">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="1f7b0-147">Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo di D3DX IMT.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-147">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="1f7b0-148">Un tensore di metrica integrato (o IMT) è una matrice 2x2 simmetrica che descrive il modo in cui un triangolo viene esteso nell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-148">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="1f7b0-149">Ogni IMT è definito da 3 float, chiamati (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-149">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="1f7b0-150">Possono essere disposte in una matrice simmetrica 2x2 come la seguente:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-150">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="1f7b0-151">È quindi possibile usare IMT per trovare la distanza tra due vettori.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-151">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="1f7b0-152">Dati due vettori v1 e V2, dove:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-152">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="1f7b0-153">La distanza tra V1 e V2 può essere calcolata come segue:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-153">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="1f7b0-154">In altre parole, il vettore (s, t) potrebbe essere la grandezza dell'estensione in una direzione arbitraria nello spazio u-v.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-154">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="1f7b0-155">In questo caso, il vettore s corrisponde a una direzione dal primo al secondo vertice e t è il prodotto incrociato di Normal e s.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-155">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="1f7b0-156">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-156">For instance:</span></span>


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



<span data-ttu-id="1f7b0-157">Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo di D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-157">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="1f7b0-158">Specificare direttamente i dati di IMT se si vuole controllare il modo in cui lo spazio di trama viene allocato ai singoli triangoli.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-158">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="1f7b0-159">In questo modo, allocare più area nell'Atlante a aree importanti di una mesh (ad esempio, il volto di un carattere o il logo toracico o le aree di una scena vicino a walking-path).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-159">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="1f7b0-160">Specificando gli IMT che sono multipli della matrice di identità, i triangoli risultanti verranno ridimensionati in modo uniforme nello spazio di trama.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-160">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="1f7b0-161">Ad esempio, data una mappa normale ad alta risoluzione, è possibile calcolare IMT per fornire più spazio di trama a aree con un segnale di frequenza superiore nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-161">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="1f7b0-162">I triangoli "flat", che sono mappati a aree costanti della mappa normale originale, riceveranno uno spazio di trama minore.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-162">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="1f7b0-163">I triangoli che contengono una grande quantità di dettagli della mappa normale riceveranno più area di trama nel risultato finale.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-163">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="1f7b0-164">È quindi possibile ricampionare la mappa normale in una trama più piccola, ma mantenere i dettagli, oppure è possibile ricalcolare la mappa normale con il mapping UV più ottimale.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-164">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="1f7b0-165">Utilizzo di dati adiacenza per le pieghe specificate dall'utente</span><span class="sxs-lookup"><span data-stu-id="1f7b0-165">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="1f7b0-166">Le informazioni adiacenza definite dall'utente possono essere fornite alla funzione di partizionamento per descrivere le pieghe predefinite nella rete e quindi definire un limite del grafico tra i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-166">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="1f7b0-167">Si tratta di un modo semplice per consentire al chiamante di specificare il proprio partizionamento del grafico come input nell'algoritmo, che consente di perfezionare ulteriormente i grafici in modo da portare l'estensione al di sotto del valore massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-167">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="1f7b0-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="1f7b0-168">Example</span></span>

<span data-ttu-id="1f7b0-169">Questo esempio illustra come usare le API UVAtlas e il Visualizzatore DirectX (Dxviewer.exe) per individuare e correggere le discontinuità nel modello che può influire in modo significativo sulle dimensioni dell'Atlante della trama.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-169">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="1f7b0-170">È possibile ottenere Dxviewer.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-170">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="1f7b0-171">Dxviewer.exe è stata rimossa da DirectX SDK dopo la versione agosto 2009, quindi per ottenerla è necessario almeno l'SDK di DirectX 2009 di agosto.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-171">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="1f7b0-172">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-172">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="1f7b0-173">Si supponga di iniziare con un modello nel software di generazione del contenuto preferito (in questo esempio viene usato un modello Head Nano creato in Maya).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-173">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="1f7b0-174">Esportare il modello con trama in un file con estensione x e creare un Atlante di trama con D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-174">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="1f7b0-175">L'Atlante di trama risultante avrà un aspetto simile a quello illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-175">The resulting texture atlas would look something like the following illustration.</span></span>

![illustrazione di un atlante per un modello nano](images/uvatlas5.jpg)

<span data-ttu-id="1f7b0-177">L'Atlante è costituito da 22 grafici e da un tratto massimo di 0,994.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-177">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="1f7b0-178">A questo punto, esaminare il modello con trama per vedere il modo in cui viene eseguito il mapping tra l'Atlante della trama e la geometria.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-178">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="1f7b0-179">A tale scopo, caricare il modello nello strumento Visualizzatore:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-179">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="1f7b0-180">Aprire lo strumento Visualizzatore da DirectX Utilities.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-180">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="1f7b0-181">Caricare il file con estensione x facendo clic sul pulsante Apri.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-181">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="1f7b0-182">Per abilitare l'opzione di visualizzazione delle pieghe, fare clic sul pulsante Visualizza e selezionare le pieghe dal popup.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-182">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="1f7b0-183">Nell'illustrazione seguente vengono mostrati gli elementi che dovrebbero essere visualizzati nello strumento Visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-183">The following illustration shows what you should see in the viewer tool.</span></span>

![illustrazione di una mesh con trama nello strumento Visualizzatore](images/uvatlas6c.jpg)

<span data-ttu-id="1f7b0-185">Ogni riga è una piega che rappresenta un bordo adiacente tra due grafici nell'Atlante della trama.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-185">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="1f7b0-186">Il numero di grafici generati dall'algoritmo è causato da lievi differenze, probabilmente a causa di discontinuità nei normali.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-186">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="1f7b0-187">Queste piccole differenze possono essere ridotte mediante i dati di saldatura, ovvero forzando i dati che sono quasi uguali.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-187">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="1f7b0-188">Per saldare i normali e il skinweights:</span><span class="sxs-lookup"><span data-stu-id="1f7b0-188">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="1f7b0-189">Eseguire lo strumento DirectX Ops (dxops.exe) con la riga di comando seguente sulla mesh (sostituendo ' modelname. x ' con il nome del modello):</span><span class="sxs-lookup"><span data-stu-id="1f7b0-189">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="1f7b0-190">Ciò consente di confrontare i valori normali e skinweights e la posizione in cui si differenziano per un valore inferiore a 2,01, i dati vengono resi uguali.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-190">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="1f7b0-191">Le illustrazioni seguenti mostrano un primo sguardo per visualizzare le pieghe prima della saldatura (a sinistra) e le pieghe dopo la saldatura (a destra):</span><span class="sxs-lookup"><span data-stu-id="1f7b0-191">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![illustrazione delle pieghe prima della saldatura](images/uvatlas6a.jpg)![illustrazione delle pieghe dopo la saldatura](images/uvatlas6b.jpg)

<span data-ttu-id="1f7b0-194">Figura 7: rimozione di pieghe mediante saldatura</span><span class="sxs-lookup"><span data-stu-id="1f7b0-194">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="1f7b0-195">In questo esempio, la saldatura ha rimosso 86 vertici dalla mesh di input.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-195">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="1f7b0-196">Con un minor numero di pieghe nella rete, è possibile rigenerare l'Atlante, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-196">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![illustrazione del nuovo Atlante con le pieghe rimosse](images/uvatlas8.jpg)

<span data-ttu-id="1f7b0-198">L'Atlante dispone solo di 7 grafici e un'estensione massima di circa 0,0776.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-198">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="1f7b0-199">Il nuovo Atlante si inserisce ora in una trama più piccola (circa il 30% di dimensioni inferiori in questo esempio).</span><span class="sxs-lookup"><span data-stu-id="1f7b0-199">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="1f7b0-200">Compressione dei grafici in un Atlante</span><span class="sxs-lookup"><span data-stu-id="1f7b0-200">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="1f7b0-201">Una volta partizionata una mesh in grafici con parametri singoli, i grafici devono essere compressi in modo efficiente in un'unica mappa di trama.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-201">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="1f7b0-202">Questa operazione viene eseguita come secondo passaggio di D3DXUVAtlasCreate o può essere richiamata in modo esplicito chiamando D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-202">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="1f7b0-203">I grafici compressi sono separati da una larghezza di gronda specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-203">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="1f7b0-204">La larghezza della barra di navigazione è la quantità di separazione tra i grafici e consente l'interpolazione bilineare e il mapping MIP per evitare il rendering degli artefatti ai limiti del grafico.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-204">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="1f7b0-205">D3DX fornisce un'interfaccia per la compilazione automatica di queste grondaie. per ulteriori informazioni, vedere [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="1f7b0-205">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="1f7b0-206">Integrazione di UVAtlas nella pipeline</span><span class="sxs-lookup"><span data-stu-id="1f7b0-206">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="1f7b0-207">Oltre a essere richiamati dall'artista prima del disegno della trama, queste funzioni possono essere integrate in una pipeline grafica automatizzata.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-207">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="1f7b0-208">Ad esempio, una chiamata UVAtlas può essere eseguita automaticamente dopo l'aggiornamento di un asset, prima di eseguire una simulazione PRT o il normale passaggio di mapping.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-208">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="1f7b0-209">In questo modo si evita di dover eseguire manualmente il ripristino manuale del mapping UV di un oggetto se la topologia della mesh è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-209">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="1f7b0-210">Vedere lo [strumento di Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) , ad esempio utilizzo delle funzioni UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="1f7b0-210">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f7b0-211">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f7b0-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f7b0-212">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="1f7b0-212">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
