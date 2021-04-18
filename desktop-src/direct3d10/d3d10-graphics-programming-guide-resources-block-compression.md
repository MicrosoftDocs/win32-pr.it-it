---
description: La compressione a blocchi è una tecnica di compressione di trama per la riduzione delle dimensioni della trama.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compressione dei blocchi (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558693"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="b39ba-103">Compressione dei blocchi (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b39ba-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="b39ba-104">La compressione a blocchi è una tecnica di compressione di trama per la riduzione delle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="b39ba-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="b39ba-105">Rispetto a una trama con 32 bit per colore, una trama compressa da blocchi può essere fino al 75% di dimensioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="b39ba-106">Le applicazioni in genere riscontrano un aumento delle prestazioni quando si usa la compressione a blocchi a causa del footprint di memoria inferiore.</span><span class="sxs-lookup"><span data-stu-id="b39ba-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="b39ba-107">Con la perdita di perdite, la compressione dei blocchi funziona correttamente ed è consigliata per tutte le trame che vengono trasformate e filtrate dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b39ba-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="b39ba-108">Le trame di cui è stato eseguito il mapping direttamente alla schermata (elementi dell'interfaccia utente come icone e testo) non sono ottime scelte per la compressione perché gli artefatti sono più evidenti.</span><span class="sxs-lookup"><span data-stu-id="b39ba-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="b39ba-109">Una trama compressa a blocchi deve essere creata come un multiplo di dimensioni 4 in tutte le dimensioni e non può essere usata come output della pipeline.</span><span class="sxs-lookup"><span data-stu-id="b39ba-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="b39ba-110">Funzionamento della compressione dei blocchi</span><span class="sxs-lookup"><span data-stu-id="b39ba-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="b39ba-111">Archiviazione di dati non compressi</span><span class="sxs-lookup"><span data-stu-id="b39ba-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="b39ba-112">Archiviazione di dati compressi</span><span class="sxs-lookup"><span data-stu-id="b39ba-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="b39ba-113">Uso della compressione a blocchi</span><span class="sxs-lookup"><span data-stu-id="b39ba-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="b39ba-114">Dimensioni virtuali rispetto alle dimensioni fisiche</span><span class="sxs-lookup"><span data-stu-id="b39ba-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="b39ba-115">Algoritmi di compressione</span><span class="sxs-lookup"><span data-stu-id="b39ba-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="b39ba-116">BC1</span><span class="sxs-lookup"><span data-stu-id="b39ba-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="b39ba-117">RB2</span><span class="sxs-lookup"><span data-stu-id="b39ba-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="b39ba-118">BC3</span><span class="sxs-lookup"><span data-stu-id="b39ba-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="b39ba-119">BC4</span><span class="sxs-lookup"><span data-stu-id="b39ba-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="b39ba-120">BC5</span><span class="sxs-lookup"><span data-stu-id="b39ba-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="b39ba-121">Conversione del formato con Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="b39ba-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="b39ba-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b39ba-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="b39ba-123">Funzionamento della compressione dei blocchi</span><span class="sxs-lookup"><span data-stu-id="b39ba-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="b39ba-124">La compressione a blocchi è una tecnica che consente di ridurre la quantità di memoria necessaria per archiviare i dati dei colori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="b39ba-125">Archiviando alcuni colori nelle dimensioni originali e altri colori utilizzando uno schema di codifica, è possibile ridurre notevolmente la quantità di memoria necessaria per archiviare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b39ba-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="b39ba-126">Poiché l'hardware decodifica automaticamente i dati compressi, non si verifica alcuna riduzione delle prestazioni per l'utilizzo di trame compresse.</span><span class="sxs-lookup"><span data-stu-id="b39ba-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="b39ba-127">Per informazioni sul funzionamento della compressione, vedere i due esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b39ba-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="b39ba-128">Nel primo esempio viene illustrata la quantità di memoria utilizzata per l'archiviazione di dati non compressi; nel secondo esempio viene descritta la quantità di memoria utilizzata per l'archiviazione dei dati compressi.</span><span class="sxs-lookup"><span data-stu-id="b39ba-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="b39ba-129">Archiviazione di dati non compressi</span><span class="sxs-lookup"><span data-stu-id="b39ba-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="b39ba-130">La figura seguente rappresenta una trama 4 × 4 non compressa.</span><span class="sxs-lookup"><span data-stu-id="b39ba-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="b39ba-131">Si supponga che ogni colore contenga un solo componente a colori (rosso per l'istanza) e che sia archiviato in un byte di memoria.</span><span class="sxs-lookup"><span data-stu-id="b39ba-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![illustrazione di una trama non compressa 4x4](images/d3d10-block-compress-1.png)

<span data-ttu-id="b39ba-133">I dati non compressi sono disposti in memoria in sequenza e richiedono 16 byte, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![illustrazione dei dati non compressi nella memoria sequenziale](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="b39ba-135">Archiviazione di dati compressi</span><span class="sxs-lookup"><span data-stu-id="b39ba-135">Storing Compressed Data</span></span>

<span data-ttu-id="b39ba-136">Ora che è stata rilevata la quantità di memoria utilizzata da un'immagine non compressa, esaminare la quantità di memoria salvata da un'immagine compressa.</span><span class="sxs-lookup"><span data-stu-id="b39ba-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="b39ba-137">Il formato di compressione [BC1](#bc1) archivia 2 colori (1 byte ciascuno) e indici a 16 3 bit (48 bit o 6 byte) usati per interpolare i colori originali nella trama, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![illustrazione del formato di compressione BC1](images/d3d10-block-compress-3.png)

<span data-ttu-id="b39ba-139">Lo spazio totale necessario per archiviare i dati compressi è di 8 byte, che corrisponde a un risparmio di memoria pari al 50% rispetto all'esempio non compresso.</span><span class="sxs-lookup"><span data-stu-id="b39ba-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="b39ba-140">Il risparmio è ancora maggiore quando viene usato più di un componente colore.</span><span class="sxs-lookup"><span data-stu-id="b39ba-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="b39ba-141">Il notevole risparmio di memoria offerto dalla compressione dei blocchi può comportare un aumento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b39ba-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="b39ba-142">Questa prestazione comporta il costo della qualità dell'immagine (a causa dell'interpolazione dei colori); Tuttavia, la qualità inferiore spesso non è evidente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="b39ba-143">Nella sezione successiva viene illustrato come Direct3D 10 semplifica l'utilizzo della compressione a blocchi nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="b39ba-144">Uso della compressione a blocchi</span><span class="sxs-lookup"><span data-stu-id="b39ba-144">Using Block Compression</span></span>

<span data-ttu-id="b39ba-145">Creare una trama compressa a blocchi come una trama non compressa (vedere [creare una trama da un file) con](d3d10-graphics-programming-guide-resources-creating-textures.md)la differenza che si specifica un formato compresso a blocchi.</span><span class="sxs-lookup"><span data-stu-id="b39ba-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="b39ba-146">Successivamente, creare una visualizzazione per associare la trama alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b39ba-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="b39ba-147">Poiché una trama compressa a blocchi può essere usata solo come input per una fase shader, è necessario creare una visualizzazione delle risorse dello shader chiamando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="b39ba-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="b39ba-148">Usare una trama compressa a blocchi nello stesso modo in cui si usa una trama non compressa.</span><span class="sxs-lookup"><span data-stu-id="b39ba-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="b39ba-149">Se l'applicazione otterrà un puntatore di memoria per i dati compressi in blocchi, è necessario tenere in considerazione la spaziatura della memoria in un mipmap che fa sì che le dimensioni dichiarate differiscano dalle dimensioni effettive.</span><span class="sxs-lookup"><span data-stu-id="b39ba-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="b39ba-150">Dimensioni virtuali rispetto alle dimensioni fisiche</span><span class="sxs-lookup"><span data-stu-id="b39ba-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="b39ba-151">Se si dispone di un codice dell'applicazione che usa un puntatore di memoria per esaminare la memoria di una trama compressa a blocchi, è necessario tenere presente una considerazione importante che potrebbe richiedere una modifica nel codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="b39ba-152">Una trama compressa a blocchi deve essere un multiplo di 4 in tutte le dimensioni perché gli algoritmi di compressione a blocchi operano su blocchi di Texel 4x4.</span><span class="sxs-lookup"><span data-stu-id="b39ba-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="b39ba-153">Si tratta di un problema per un mipmap le cui dimensioni iniziali sono divisibili per 4, ma i livelli subdivisi non lo sono.</span><span class="sxs-lookup"><span data-stu-id="b39ba-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="b39ba-154">Il diagramma seguente mostra la differenza di area tra la dimensione virtuale (dichiarata) e la dimensione fisica (effettiva) di ogni livello di mipmap.</span><span class="sxs-lookup"><span data-stu-id="b39ba-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![diagramma dei livelli di mipmap non compressi e compressi](images/d3d10-block-compress-pad.png)

<span data-ttu-id="b39ba-156">Il lato sinistro del diagramma mostra le dimensioni del livello mipmap generate per una trama 60 × 40 non compressa.</span><span class="sxs-lookup"><span data-stu-id="b39ba-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="b39ba-157">Le dimensioni di primo livello sono tratte dalla chiamata API che genera la trama; ogni livello successivo è la metà delle dimensioni del livello precedente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="b39ba-158">Per una trama non compressa, non esiste alcuna differenza tra le dimensioni virtuali (dichiarate) e le dimensioni fisiche (effettive).</span><span class="sxs-lookup"><span data-stu-id="b39ba-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="b39ba-159">Il lato destro del diagramma mostra le dimensioni del livello mipmap generate per la stessa trama 60 × 40 con compressione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="b39ba-160">Si noti che il secondo e il terzo livello hanno riempimento della memoria per rendere i fattori di dimensioni 4 a ogni livello.</span><span class="sxs-lookup"><span data-stu-id="b39ba-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="b39ba-161">Questa operazione è necessaria in modo che gli algoritmi possano operare su blocchi di 4 × 4 Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="b39ba-162">Questo è particolarmente evidente se si considerano i livelli mipmap inferiori a 4 × 4; la dimensione di questi livelli mipmap molto piccoli verrà arrotondata al fattore più vicino di 4 quando viene allocata la memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="b39ba-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="b39ba-163">L'hardware di campionamento usa la dimensione virtuale; Quando si campiona la trama, il riempimento della memoria viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b39ba-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="b39ba-164">Per i livelli mipmap inferiori a 4 × 4, verranno usati solo i primi quattro Texel per una mappa 2 × 2 e solo il primo Texel verrà usato da un blocco 1 × 1.</span><span class="sxs-lookup"><span data-stu-id="b39ba-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="b39ba-165">Tuttavia, non esiste alcuna struttura API che espone le dimensioni fisiche (inclusa la spaziatura interna della memoria).</span><span class="sxs-lookup"><span data-stu-id="b39ba-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="b39ba-166">In breve, prestare attenzione a usare blocchi di memoria allineati quando si copiano aree che contengono dati compressi in blocchi.</span><span class="sxs-lookup"><span data-stu-id="b39ba-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="b39ba-167">Per eseguire questa operazione in un'applicazione che ottiene un puntatore di memoria, verificare che il puntatore usi il passo della superficie per tenere conto delle dimensioni della memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="b39ba-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="b39ba-168">Algoritmi di compressione</span><span class="sxs-lookup"><span data-stu-id="b39ba-168">Compression Algorithms</span></span>

<span data-ttu-id="b39ba-169">Le tecniche di compressione dei blocchi in Direct3D suddividono i dati di trama non compressi in 4 × 4 blocchi, comprimono ogni blocco e quindi archiviano i dati.</span><span class="sxs-lookup"><span data-stu-id="b39ba-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="b39ba-170">Per questo motivo, è previsto che le trame siano compresse devono avere dimensioni di trama multipli di 4.</span><span class="sxs-lookup"><span data-stu-id="b39ba-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![diagramma della compressione dei blocchi](images/d3d10-compression-1.png)

<span data-ttu-id="b39ba-172">Il diagramma precedente mostra una trama partizionata in blocchi Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="b39ba-173">Il primo blocco Mostra il layout dei 16 Texel con etichetta a-p, ma ogni blocco ha la stessa organizzazione di dati.</span><span class="sxs-lookup"><span data-stu-id="b39ba-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="b39ba-174">Direct3D implementa diversi schemi di compressione, ognuno dei quali implementa un compromesso diverso tra il numero di componenti archiviati, il numero di bit per componente e la quantità di memoria utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b39ba-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="b39ba-175">Usare questa tabella per scegliere il formato più adatto al tipo di dati e alla risoluzione dei dati più adatta all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="b39ba-176">Origine dati</span><span class="sxs-lookup"><span data-stu-id="b39ba-176">Source Data</span></span>                     | <span data-ttu-id="b39ba-177">Risoluzione della compressione dei dati (in bit)</span><span class="sxs-lookup"><span data-stu-id="b39ba-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="b39ba-178">Scegliere questo formato di compressione</span><span class="sxs-lookup"><span data-stu-id="b39ba-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="b39ba-179">Colore a tre componenti e alfa</span><span class="sxs-lookup"><span data-stu-id="b39ba-179">Three-component color and alpha</span></span> | <span data-ttu-id="b39ba-180">Color (5:6:5), Alpha (1) o nessun Alpha</span><span class="sxs-lookup"><span data-stu-id="b39ba-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="b39ba-181">BC1</span><span class="sxs-lookup"><span data-stu-id="b39ba-181">BC1</span></span>                            |
| <span data-ttu-id="b39ba-182">Colore a tre componenti e alfa</span><span class="sxs-lookup"><span data-stu-id="b39ba-182">Three-component color and alpha</span></span> | <span data-ttu-id="b39ba-183">Colore (5:6:5), Alfa (4)</span><span class="sxs-lookup"><span data-stu-id="b39ba-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="b39ba-184">RB2</span><span class="sxs-lookup"><span data-stu-id="b39ba-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="b39ba-185">Colore a tre componenti e alfa</span><span class="sxs-lookup"><span data-stu-id="b39ba-185">Three-component color and alpha</span></span> | <span data-ttu-id="b39ba-186">Colore (5:6:5), Alfa (8)</span><span class="sxs-lookup"><span data-stu-id="b39ba-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="b39ba-187">BC3</span><span class="sxs-lookup"><span data-stu-id="b39ba-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="b39ba-188">Colore di un componente</span><span class="sxs-lookup"><span data-stu-id="b39ba-188">One-component color</span></span>             | <span data-ttu-id="b39ba-189">Un componente (8)</span><span class="sxs-lookup"><span data-stu-id="b39ba-189">One component (8)</span></span>                     | [<span data-ttu-id="b39ba-190">BC4</span><span class="sxs-lookup"><span data-stu-id="b39ba-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="b39ba-191">Colore a due componenti</span><span class="sxs-lookup"><span data-stu-id="b39ba-191">Two-component color</span></span>             | <span data-ttu-id="b39ba-192">Due componenti (8:8)</span><span class="sxs-lookup"><span data-stu-id="b39ba-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="b39ba-193">BC5</span><span class="sxs-lookup"><span data-stu-id="b39ba-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="b39ba-194">BC1</span><span class="sxs-lookup"><span data-stu-id="b39ba-194">BC1</span></span>

<span data-ttu-id="b39ba-195">Usare il primo formato di compressione a blocchi (BC1) (DXGI \_ Format BC1, formato \_ \_ DXGI \_ BC1 UNORM o DXGI BC1 UNORM \_ \_ \_ \_ \_ sRGB) per archiviare dati di colore a tre componenti usando un colore 5:6:5 (5 bit in rosso, 6 bit verde, 5 bit blu).</span><span class="sxs-lookup"><span data-stu-id="b39ba-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="b39ba-196">Questo vale anche se i dati contengono anche Alfa a 1 bit.</span><span class="sxs-lookup"><span data-stu-id="b39ba-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="b39ba-197">Supponendo una trama 4 × 4 con il formato dati più grande possibile, il formato BC1 riduce la quantità di memoria richiesta da 48 byte (16 colori × 3 componenti/colore × 1 byte/componente) a 8 byte di memoria.</span><span class="sxs-lookup"><span data-stu-id="b39ba-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="b39ba-198">L'algoritmo funziona su 4 × 4 blocchi di Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="b39ba-199">Anziché archiviare 16 colori, l'algoritmo Salva due colori di riferimento (colore \_ 0 e colore \_ 1) e indici di colore a 16 2 bit (blocca a-p), come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![diagramma del layout per la compressione BC1](images/d3d10-compression-bc1.png)

<span data-ttu-id="b39ba-201">Gli indici di colore (a-p) vengono usati per cercare i colori originali da una tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="b39ba-202">La tabella dei colori contiene 4 colori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-202">The color table contains 4 colors.</span></span> <span data-ttu-id="b39ba-203">I primi due colori, ovvero colore \_ 0 e colore \_ 1, sono i colori minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="b39ba-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="b39ba-204">Gli altri due colori, colore \_ 2 e colore \_ 3, sono colori intermedi calcolati con l'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="b39ba-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="b39ba-205">Ai quattro colori vengono assegnati valori di indice a 2 bit che verranno salvati nei blocchi a-p.</span><span class="sxs-lookup"><span data-stu-id="b39ba-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="b39ba-206">Infine, ognuno dei colori nei blocchi a-p viene confrontato con i quattro colori della tabella dei colori e l'indice per il colore più vicino viene archiviato nei blocchi a 2 bit.</span><span class="sxs-lookup"><span data-stu-id="b39ba-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="b39ba-207">Questo algoritmo si presta ai dati che contengono anche Alpha a 1 bit.</span><span class="sxs-lookup"><span data-stu-id="b39ba-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="b39ba-208">L'unica differenza è che color \_ 3 è impostato su 0 (che rappresenta un colore trasparente) e il colore \_ 2 è una combinazione lineare di colore \_ 0 e colore \_ 1.</span><span class="sxs-lookup"><span data-stu-id="b39ba-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b39ba-209">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b39ba-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="b39ba-210">Questo formato è disponibile sia in Direct3D 9 che in 10.</span><span class="sxs-lookup"><span data-stu-id="b39ba-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="b39ba-211">In Direct3D 9 il formato BC1 è denominato D3DFMT_DXT1.</span><span class="sxs-lookup"><span data-stu-id="b39ba-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="b39ba-212">In Direct3D 10 il formato BC1 è rappresentato da DXGI_FORMAT_BC1_UNORM o DXGI_FORMAT_BC1_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="b39ba-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="b39ba-213">RB2</span><span class="sxs-lookup"><span data-stu-id="b39ba-213">BC2</span></span>

<span data-ttu-id="b39ba-214">Usare il formato BC2 (DXGI \_ Format \_ BC2 \_ senza tipo, DXGI Format BC2 UNORM o DXGI BC2 UNORM \_ \_ \_ \_ \_ \_ sRGB) per archiviare i dati che contengono i dati di colore e alfa con coerenza Bassi (usare [BC3](#bc3) per dati alfa altamente coerenti).</span><span class="sxs-lookup"><span data-stu-id="b39ba-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="b39ba-215">Il formato BC2 archivia i dati RGB come un colore 5:6:5 (5 bit rosso, 6 bit verde, 5 bit blu) e alfa come valore separato a 4 bit.</span><span class="sxs-lookup"><span data-stu-id="b39ba-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="b39ba-216">Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.</span><span class="sxs-lookup"><span data-stu-id="b39ba-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="b39ba-217">Il formato BC2 archivia i colori con lo stesso numero di bit e il layout dei dati del formato [BC1](#bc1) ; Tuttavia, BC2 richiede altri 64 bit di memoria per archiviare i dati alfa, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![diagramma del layout per la compressione BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b39ba-219">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b39ba-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="b39ba-220">Questo formato è disponibile sia in Direct3D 9 che in 10.</span><span class="sxs-lookup"><span data-stu-id="b39ba-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="b39ba-221">In Direct3D 9 il formato BC2 è denominato D3DFMT_DXT2 e D3DFMT_DXT3.</span><span class="sxs-lookup"><span data-stu-id="b39ba-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="b39ba-222">In Direct3D 10 il formato BC2 è rappresentato da DXGI_FORMAT_BC2_UNORM o DXGI_FORMAT_BC2_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="b39ba-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="b39ba-223">BC3</span><span class="sxs-lookup"><span data-stu-id="b39ba-223">BC3</span></span>

<span data-ttu-id="b39ba-224">Usare il formato BC3 (DXGI \_ Format \_ BC3, formato \_ DXGI \_ BC3 UNORM o DXGI BC3 UNORM \_ \_ \_ \_ \_ sRGB) per archiviare dati di colore altamente coerenti (usare [BC2](#bc2) con dati alfa meno coerenti).</span><span class="sxs-lookup"><span data-stu-id="b39ba-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="b39ba-225">Il formato BC3 archivia i dati relativi ai colori utilizzando il colore 5:6:5 (5 bit rosso, 6 bit verde, 5 bit blu) e i dati alfa utilizzando un solo byte.</span><span class="sxs-lookup"><span data-stu-id="b39ba-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="b39ba-226">Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.</span><span class="sxs-lookup"><span data-stu-id="b39ba-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="b39ba-227">Il formato BC3 archivia i colori con lo stesso numero di bit e il layout dei dati del formato [BC1](#bc1) ; Tuttavia, BC3 richiede altri 64 bit di memoria per archiviare i dati alfa.</span><span class="sxs-lookup"><span data-stu-id="b39ba-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="b39ba-228">Il formato BC3 gestisce Alpha archiviando due valori di riferimento e interpolando tra di essi, in modo analogo al modo in cui BC1 archivia il colore RGB.</span><span class="sxs-lookup"><span data-stu-id="b39ba-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="b39ba-229">L'algoritmo funziona su 4 × 4 blocchi di Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="b39ba-230">Anziché archiviare 16 valori alfa, l'algoritmo archivia 2 alfa di riferimento (Alpha \_ 0 e Alpha \_ 1) e indici di colore a 16 3 bit (da Alpha a a p), come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![diagramma del layout per la compressione BC3](images/d3d10-compression-bc3.png)

<span data-ttu-id="b39ba-232">Il formato BC3 utilizza gli indici alfa (a-p) per cercare i colori originali da una tabella di ricerca che contiene 8 valori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="b39ba-233">I primi due valori, ovvero Alpha \_ 0 e Alpha \_ 1, sono i valori minimo e massimo. gli altri sei valori intermedi vengono calcolati usando l'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="b39ba-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="b39ba-234">L'algoritmo determina il numero di valori alfa interpolati esaminando i due valori alfa di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b39ba-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="b39ba-235">Se alfa \_ 0 è maggiore di alfa \_ 1, BC3 interpolano 6 valori alfa; in caso contrario, esegue l'interpolazione 4.</span><span class="sxs-lookup"><span data-stu-id="b39ba-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="b39ba-236">Quando BC3 interpola solo 4 valori alfa, imposta due valori alfa aggiuntivi (0 per completamente trasparente e 255 per l'intero opaco).</span><span class="sxs-lookup"><span data-stu-id="b39ba-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="b39ba-237">BC3 comprime i valori alfa nell'area di Texel 4 × 4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrisponde maggiormente all'alfa originale per un dato Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b39ba-238">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b39ba-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="b39ba-239">In Direct3D 9 il formato BC3 è denominato D3DFMT_DXT4 e D3DFMT_DXT5.</span><span class="sxs-lookup"><span data-stu-id="b39ba-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="b39ba-240">In Direct3D 10 il formato BC3 è rappresentato da DXGI_FORMAT_BC3_UNORM o DXGI_FORMAT_BC3_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="b39ba-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="b39ba-241">BC4</span><span class="sxs-lookup"><span data-stu-id="b39ba-241">BC4</span></span>

<span data-ttu-id="b39ba-242">Usare il formato BC4 per archiviare i dati dei colori di un componente usando 8 bit per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="b39ba-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="b39ba-243">A causa della maggiore precisione (rispetto a [BC1](#bc1)), BC4 è la soluzione ideale per l'archiviazione di dati a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1 usando il formato DXGI \_ \_ BC4 \_ UNORM e \[ da-1 a + 1 \] usando il formato DXGI \_ BC4 il \_ \_ formato russamento.</span><span class="sxs-lookup"><span data-stu-id="b39ba-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="b39ba-244">Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 16 byte (16 colori × 1 componenti/colore × 1 byte/componente) a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="b39ba-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="b39ba-245">L'algoritmo funziona su 4 × 4 blocchi di Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="b39ba-246">Anziché archiviare 16 colori, l'algoritmo archivia 2 colori di riferimento (rosso \_ 0 e rosso \_ 1) e indici di colore a 16 3 bit (da rosso a a p rosso), come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![diagramma del layout per la compressione BC4](images/d3d10-compression-bc4.png)

<span data-ttu-id="b39ba-248">L'algoritmo utilizza gli indici a 3 bit per cercare i colori di una tabella dei colori che contiene 8 colori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="b39ba-249">I primi due colori, Rossi \_ 0 e rossi \_ 1, sono i colori minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="b39ba-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="b39ba-250">L'algoritmo calcola i colori rimanenti utilizzando l'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="b39ba-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="b39ba-251">L'algoritmo determina il numero di valori dei colori interpolati esaminando i due valori di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b39ba-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="b39ba-252">Se il colore rosso \_ 0 è maggiore di quello rosso \_ 1, BC4 interpola i 6 valori dei colori; in caso contrario, interpola 4.</span><span class="sxs-lookup"><span data-stu-id="b39ba-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="b39ba-253">Quando BC4 esegue l'interpolazione solo di 4 valori di colore, imposta due valori di colore aggiuntivi (0,0 f per completamente trasparente e 1,0 f per l'opacità completa).</span><span class="sxs-lookup"><span data-stu-id="b39ba-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="b39ba-254">BC4 comprime i valori alfa nell'area di Texel 4 × 4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrispondono maggiormente all'alfa originale per un dato Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="b39ba-255">\_UNORM BC4</span><span class="sxs-lookup"><span data-stu-id="b39ba-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="b39ba-256">BC4 \_ russare</span><span class="sxs-lookup"><span data-stu-id="b39ba-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="b39ba-257">\_UNORM BC4</span><span class="sxs-lookup"><span data-stu-id="b39ba-257">BC4\_UNORM</span></span>

<span data-ttu-id="b39ba-258">L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="b39ba-259">Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="b39ba-260">BC4 \_ russare</span><span class="sxs-lookup"><span data-stu-id="b39ba-260">BC4\_SNORM</span></span>

<span data-ttu-id="b39ba-261">Il \_ formato DXGI \_ BC4 \_ russa è identico, ad eccezione del fatto che i dati sono codificati in un intervallo di russamento e quando vengono interpolati 4 valori di colore.</span><span class="sxs-lookup"><span data-stu-id="b39ba-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="b39ba-262">L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="b39ba-263">Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="b39ba-264">BC5</span><span class="sxs-lookup"><span data-stu-id="b39ba-264">BC5</span></span>

<span data-ttu-id="b39ba-265">Usare il formato BC5 per archiviare i dati di colore a due componenti usando 8 bit per ogni colore.</span><span class="sxs-lookup"><span data-stu-id="b39ba-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="b39ba-266">A causa della maggiore precisione (rispetto a [BC1](#bc1)), BC5 è la soluzione ideale per l'archiviazione di dati a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1 usando il formato DXGI \_ \_ BC5 \_ UNORM e \[ da-1 a + 1 \] usando il formato DXGI \_ BC5 il \_ \_ formato russamento.</span><span class="sxs-lookup"><span data-stu-id="b39ba-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="b39ba-267">Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 32 byte (16 colori × 2 componenti/colore × 1 byte/componente) a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="b39ba-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="b39ba-268">L'algoritmo funziona su 4 × 4 blocchi di Texel.</span><span class="sxs-lookup"><span data-stu-id="b39ba-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="b39ba-269">Anziché archiviare 16 colori per entrambi i componenti, l'algoritmo archivia 2 colori di riferimento per ogni componente (rosso \_ 0, rosso \_ 1, verde \_ 0 e verde \_ 1) e indici di colore a 16 3 bit per ogni componente (da rosso a a rosso p e da verde a a p verde), come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![diagramma del layout per la compressione BC5](images/d3d10-compression-bc5.png)

<span data-ttu-id="b39ba-271">L'algoritmo utilizza gli indici a 3 bit per cercare i colori di una tabella dei colori che contiene 8 colori.</span><span class="sxs-lookup"><span data-stu-id="b39ba-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="b39ba-272">I primi due colori, Rossi \_ 0 e rossi \_ 1 (o verde \_ 0 e verde \_ 1), sono i colori minimo e massimo.</span><span class="sxs-lookup"><span data-stu-id="b39ba-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="b39ba-273">L'algoritmo calcola i colori rimanenti utilizzando l'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="b39ba-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="b39ba-274">L'algoritmo determina il numero di valori dei colori interpolati esaminando i due valori di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b39ba-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="b39ba-275">Se il colore rosso \_ 0 è maggiore di quello rosso \_ 1, BC5 interpola i 6 valori dei colori; in caso contrario, interpola 4.</span><span class="sxs-lookup"><span data-stu-id="b39ba-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="b39ba-276">Quando BC5 esegue l'interpolazione solo di 4 valori di colore, imposta i restanti due valori di colore su 0,0 f e 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="b39ba-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="b39ba-277">\_UNORM BC5</span><span class="sxs-lookup"><span data-stu-id="b39ba-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="b39ba-278">BC5 \_ russare</span><span class="sxs-lookup"><span data-stu-id="b39ba-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="b39ba-279">\_UNORM BC5</span><span class="sxs-lookup"><span data-stu-id="b39ba-279">BC5\_UNORM</span></span>

<span data-ttu-id="b39ba-280">L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="b39ba-281">I calcoli per i componenti verdi sono simili.</span><span class="sxs-lookup"><span data-stu-id="b39ba-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="b39ba-282">Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="b39ba-283">BC5 \_ russare</span><span class="sxs-lookup"><span data-stu-id="b39ba-283">BC5\_SNORM</span></span>

<span data-ttu-id="b39ba-284">Il \_ formato DXGI \_ BC5 \_ russa è identico, ad eccezione del fatto che i dati sono codificati nell'intervallo di russamento e quando 4 valori di dati vengono interpolati, i due valori aggiuntivi sono-1.0 f e 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="b39ba-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="b39ba-285">L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b39ba-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="b39ba-286">I calcoli per i componenti verdi sono simili.</span><span class="sxs-lookup"><span data-stu-id="b39ba-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="b39ba-287">Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="b39ba-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="b39ba-288">Conversione del formato con Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="b39ba-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="b39ba-289">Direct3D 10,1 Abilita le copie tra trame tipizzate in modo prestrutturato e trame compresse con le stesse larghezze di bit.</span><span class="sxs-lookup"><span data-stu-id="b39ba-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="b39ba-290">Le funzioni che possono eseguire questa operazione sono [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="b39ba-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="b39ba-291">A partire da Direct3D 10,1, è possibile usare [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) per copiare alcuni tipi di formato.</span><span class="sxs-lookup"><span data-stu-id="b39ba-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="b39ba-292">Questo tipo di operazione di copia esegue un tipo di conversione del formato che reinterpreta i dati delle risorse con un tipo di formato diverso.</span><span class="sxs-lookup"><span data-stu-id="b39ba-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="b39ba-293">Si consideri questo esempio in cui viene illustrata la differenza tra la reinterpretazione dei dati e il comportamento di un tipo più tipico di conversione:</span><span class="sxs-lookup"><span data-stu-id="b39ba-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="b39ba-294">Per interpretare ' f ' come tipo di ' u ', usare [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span><span class="sxs-lookup"><span data-stu-id="b39ba-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="b39ba-295">Nella riinterpretazione precedente, il valore sottostante dei dati non cambia; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta il float come Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="b39ba-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="b39ba-296">Per eseguire il tipo di conversione più comune, usare l'assegnazione:</span><span class="sxs-lookup"><span data-stu-id="b39ba-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="b39ba-297">Nella conversione precedente, il valore sottostante dei dati viene modificato.</span><span class="sxs-lookup"><span data-stu-id="b39ba-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="b39ba-298">Nella tabella seguente sono elencati i formati di origine e di destinazione consentiti che è possibile utilizzare in questo tipo di riinterpretazione della conversione del formato.</span><span class="sxs-lookup"><span data-stu-id="b39ba-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="b39ba-299">È necessario codificare correttamente i valori affinché la riinterpretazione funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="b39ba-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="b39ba-300">Larghezza bit</span><span class="sxs-lookup"><span data-stu-id="b39ba-300">Bit Width</span></span> | <span data-ttu-id="b39ba-301">Risorsa non compressa</span><span class="sxs-lookup"><span data-stu-id="b39ba-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="b39ba-302">Risorsa Block-Compressed</span><span class="sxs-lookup"><span data-stu-id="b39ba-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b39ba-303">32</span><span class="sxs-lookup"><span data-stu-id="b39ba-303">32</span></span>        | <span data-ttu-id="b39ba-304">\_Formato DXGI \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="b39ba-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="b39ba-305">\_Formato DXGI \_ R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="b39ba-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="b39ba-306">\_Formato DXGI \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="b39ba-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="b39ba-307">64</span><span class="sxs-lookup"><span data-stu-id="b39ba-307">64</span></span>        | <span data-ttu-id="b39ba-308">\_Formato DXGI \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="b39ba-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="b39ba-309">\_Formato DXGI \_ R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="b39ba-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="b39ba-310">\_Formato DXGI \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="b39ba-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="b39ba-311">\_Formato DXGI \_ R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="b39ba-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="b39ba-312">\_Formato DXGI \_ BC1 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="b39ba-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="b39ba-313">\_Formato DXGI \_ BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b39ba-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="b39ba-314">DXGI \_ Format \_ BC4 \_ russar</span><span class="sxs-lookup"><span data-stu-id="b39ba-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="b39ba-315">128</span><span class="sxs-lookup"><span data-stu-id="b39ba-315">128</span></span>       | <span data-ttu-id="b39ba-316">\_Formato DXGI \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="b39ba-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="b39ba-317">\_Formato DXGI \_ R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="b39ba-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="b39ba-318">\_Formato DXGI \_ BC2 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="b39ba-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="b39ba-319">\_Formato DXGI \_ BC3 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="b39ba-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="b39ba-320">\_Formato DXGI \_ BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="b39ba-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="b39ba-321">DXGI \_ Format \_ BC5 \_ russar</span><span class="sxs-lookup"><span data-stu-id="b39ba-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b39ba-322">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b39ba-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b39ba-323">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b39ba-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
