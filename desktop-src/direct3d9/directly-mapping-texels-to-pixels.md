---
description: Quando si esegue il rendering dell'output 2D usando i vertici pre-trasformati, è necessario prestare attenzione per assicurarsi che ogni area di Texel corrisponda correttamente a un'area a singolo pixel. in caso contrario, può verificarsi una distorsione della trama.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapping diretto dei Texel ai pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225422"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="88d4d-103">Mapping diretto dei Texel ai pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88d4d-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="88d4d-104">Quando si esegue il rendering dell'output 2D usando i vertici pre-trasformati, è necessario prestare attenzione per assicurarsi che ogni area di Texel corrisponda correttamente a un'area a singolo pixel. in caso contrario, può verificarsi una distorsione della trama.</span><span class="sxs-lookup"><span data-stu-id="88d4d-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="88d4d-105">Comprendendo le nozioni di base del processo seguito da Direct3D durante la rasterizzazione e il texturing dei triangoli, è possibile garantire che l'applicazione Direct3D esegua correttamente il rendering dell'output 2D.</span><span class="sxs-lookup"><span data-stu-id="88d4d-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![illustrazione di una visualizzazione della risoluzione 6x6](images/maptex-fig1.png)

<span data-ttu-id="88d4d-107">Il diagramma precedente Mostra i pixel modellati come quadrati.</span><span class="sxs-lookup"><span data-stu-id="88d4d-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="88d4d-108">In realtà, tuttavia, i pixel sono punti, non quadrati.</span><span class="sxs-lookup"><span data-stu-id="88d4d-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="88d4d-109">Ogni quadrato nel diagramma precedente indica l'area illuminata dal pixel, ma un pixel è sempre solo un punto al centro di un quadrato.</span><span class="sxs-lookup"><span data-stu-id="88d4d-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="88d4d-110">Questa distinzione, sebbene apparentemente piccola, è importante.</span><span class="sxs-lookup"><span data-stu-id="88d4d-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="88d4d-111">Il diagramma seguente illustra una migliore illustrazione della stessa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="88d4d-111">A better illustration of the same display is shown in the following diagram.</span></span>

![illustrazione di una visualizzazione costituita da pixel](images/maptex-fig2.png)

<span data-ttu-id="88d4d-113">Il diagramma precedente Mostra correttamente ogni pixel fisico come punto al centro di ciascuna cella.</span><span class="sxs-lookup"><span data-stu-id="88d4d-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="88d4d-114">La coordinata dello spazio dello schermo (0,0) si trova direttamente sul pixel in alto a sinistra e quindi al centro della cella in alto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="88d4d-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="88d4d-115">L'angolo superiore sinistro dello schermo è quindi in (-0,5-0,5) perché è 0,5 celle a sinistra e 0,5 celle verso l'alto dal pixel superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="88d4d-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="88d4d-116">Direct3D eseguirà il rendering di un quad con angoli in (0, 0) e (4, 4), come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="88d4d-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![illustrazione di una struttura di un quad non rasterizzato tra (0, 0) e (4, 4)](images/maptex-fig3.png)

<span data-ttu-id="88d4d-118">L'illustrazione precedente Mostra la posizione in cui il quad matematico è correlato alla visualizzazione, ma non Mostra il risultato del Quad quando Direct3D lo Rasterizza e lo invia alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="88d4d-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="88d4d-119">Infatti, non è possibile che una visualizzazione raster riempia il quad esattamente come mostrato perché i bordi del quad non coincidono con i limiti tra le celle dei pixel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="88d4d-120">In altre parole, poiché ogni pixel può visualizzare solo un singolo colore, ogni cella pixel viene riempita con un solo colore. Se lo schermo fosse il rendering del Quad esattamente come illustrato, le celle dei pixel lungo il bordo del quadre dovrebbero mostrare due colori distinti, ovvero blu, in cui il quadrato e il bianco sono visibili solo sullo sfondo.</span><span class="sxs-lookup"><span data-stu-id="88d4d-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="88d4d-121">Al contrario, l'hardware grafico viene utilizzato per determinare i pixel da riempire per approssimare il quad.</span><span class="sxs-lookup"><span data-stu-id="88d4d-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="88d4d-122">Questo processo è denominato rasterizzazione ed è descritto in dettaglio nelle [regole di rasterizzazione (Direct3D 9)](rasterization-rules.md).</span><span class="sxs-lookup"><span data-stu-id="88d4d-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="88d4d-123">Per questo particolare caso, il quad rasterizzato è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="88d4d-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![illustrazione di un quad non con trama disegnato da (0,0) a (4, 4)](images/maptex-fig4.png)

<span data-ttu-id="88d4d-125">Si noti che il quad passato a Direct3D ha gli angoli in (0,0) e (4, 4), ma l'output rasterizzato (l'illustrazione precedente) ha gli angoli in (-0,5,-0,5) e (3.5, 3.5).</span><span class="sxs-lookup"><span data-stu-id="88d4d-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="88d4d-126">Confrontare le due illustrazioni precedenti per le differenze di rendering.</span><span class="sxs-lookup"><span data-stu-id="88d4d-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="88d4d-127">È possibile osservare che il rendering effettivamente visualizzato è la dimensione corretta, ma è stato spostato da-0,5 celle nelle direzioni x e y.</span><span class="sxs-lookup"><span data-stu-id="88d4d-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="88d4d-128">Tuttavia, fatta eccezione per le tecniche di campionamento multiplo, questa è la migliore approssimazione possibile al quad.</span><span class="sxs-lookup"><span data-stu-id="88d4d-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="88d4d-129">Vedere l' [esempio antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) per una copertura completa del campionamento multiplo. Tenere presente che se il rasterizzatore riempie ogni cella il quad, l'area risultante sarà della dimensione 5 x 5 anziché quella desiderata 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="88d4d-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="88d4d-130">Se si presuppone che le coordinate dello schermo provengano dall'angolo superiore sinistro della griglia di visualizzazione anziché dal pixel superiore sinistro, il quad viene visualizzato esattamente come previsto.</span><span class="sxs-lookup"><span data-stu-id="88d4d-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="88d4d-131">Tuttavia, la differenza diventa evidente quando al quad viene assegnata una trama.</span><span class="sxs-lookup"><span data-stu-id="88d4d-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="88d4d-132">Nella figura seguente viene illustrata la trama 4 x 4 di cui si eseguirà il mapping direttamente nel quad.</span><span class="sxs-lookup"><span data-stu-id="88d4d-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![illustrazione di una trama 4x4](images/maptex-fig5.png)

<span data-ttu-id="88d4d-134">Poiché la trama è 4 Texel e il quad è 4 x 4 pixel, è possibile prevedere che il quad con trama appaia esattamente come la trama, indipendentemente dalla posizione sullo schermo in cui viene disegnato il quad.</span><span class="sxs-lookup"><span data-stu-id="88d4d-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="88d4d-135">Tuttavia, questo non è il caso. anche le piccole modifiche alla posizione influiscono sulla modalità di visualizzazione della trama.</span><span class="sxs-lookup"><span data-stu-id="88d4d-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="88d4d-136">Nell'illustrazione seguente viene mostrato come un quad tra (0, 0) e (4, 4) viene visualizzato dopo essere stato rasterizzato e con trama.</span><span class="sxs-lookup"><span data-stu-id="88d4d-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![illustrazione di un quad con trama disegnato da (0, 0) e (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="88d4d-138">Il quad disegnato nell'illustrazione precedente mostra l'output con trama (con una modalità di filtro lineare e una modalità di indirizzamento del morsetto) con il contorno rasterizzato sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="88d4d-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="88d4d-139">Nella parte restante di questo articolo viene spiegato esattamente il motivo per cui l'output è simile al modo in cui viene eseguito anziché sembrare la trama, ma per coloro che desiderano la soluzione qui è: i bordi del Quad di input devono trovarsi sulle linee limite tra le celle dei pixel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="88d4d-140">Semplicemente spostando le coordinate quadre x e y per-0,5 unità, le celle Texel copriranno perfettamente le celle dei pixel e il quad potrà essere ricreato perfettamente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="88d4d-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="88d4d-141">L'ultima figura in questo argomento illustra il quad alle coordinate corrette.</span><span class="sxs-lookup"><span data-stu-id="88d4d-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="88d4d-142">I dettagli del motivo per cui l'output rasterizzato ha solo una lieve somiglianza alla trama di input sono direttamente correlati al modo in cui le trame degli esempi e degli indirizzi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="88d4d-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="88d4d-143">Di seguito si presuppone che si disponga di una conoscenza corretta dello [spazio delle coordinate di trama](texture-coordinates.md) e del [filtraggio bilineare della trama](bilinear-texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="88d4d-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="88d4d-144">Tornando all'analisi dello strano output dei pixel, è opportuno tracciare il colore di output nella pixel shader: la pixel shader viene chiamata per ogni pixel selezionato per far parte della forma rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="88d4d-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="88d4d-145">Il quad blu a tinta unita raffigurato in un'illustrazione precedente potrebbe avere uno shader particolarmente semplice:</span><span class="sxs-lookup"><span data-stu-id="88d4d-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="88d4d-146">Per il quad con trama, è necessario modificare leggermente la pixel shader:</span><span class="sxs-lookup"><span data-stu-id="88d4d-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="88d4d-147">Il codice presuppone che la trama 4 x 4 venga archiviata in texture.</span><span class="sxs-lookup"><span data-stu-id="88d4d-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="88d4d-148">Come illustrato, il campionatore di trame di Sampler è impostato in modo da eseguire filtri bilineari su texture.</span><span class="sxs-lookup"><span data-stu-id="88d4d-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="88d4d-149">Il pixel shader viene chiamato una volta per ogni pixel rasterizzato e ogni volta che il colore restituito è il colore della trama campionata in vTexCoord.</span><span class="sxs-lookup"><span data-stu-id="88d4d-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="88d4d-150">Ogni volta che viene chiamata la pixel shader, l'argomento vTexCoord viene impostato sulle coordinate di trama in corrispondenza di tale pixel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="88d4d-151">Ciò significa che lo shader sta chiedendo il campionatore di trame per il colore della trama filtrata nella posizione esatta del pixel, come descritto nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="88d4d-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![illustrazione dei percorsi di campionamento per le coordinate di trama](images/maptex-fig7.png)

<span data-ttu-id="88d4d-153">La trama (visualizzata sovrapposta) viene campionata direttamente in posizioni in pixel (visualizzate come punti neri).</span><span class="sxs-lookup"><span data-stu-id="88d4d-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="88d4d-154">Le coordinate di trama non sono interessate dalla rasterizzazione (rimangono nello schermo proiettato-spazio del Quad originale).</span><span class="sxs-lookup"><span data-stu-id="88d4d-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="88d4d-155">I punti neri mostrano dove si trovano i pixel di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="88d4d-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="88d4d-156">Le coordinate di trama in ogni pixel sono facilmente determinate mediante l'interpolazione delle coordinate archiviate in ogni vertice: il pixel in corrispondenza di (0, 0) coincide con il vertice in corrispondenza di (0, 0); Pertanto, le coordinate di trama in quel pixel sono semplicemente le coordinate di trama archiviate in quel vertice, UV (0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="88d4d-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="88d4d-157">Per il pixel in corrispondenza di (3, 1), le coordinate interpolate sono UV (0,75, 0,25) perché il pixel si trova a tre quarti della larghezza della trama e un quarto dell'altezza.</span><span class="sxs-lookup"><span data-stu-id="88d4d-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="88d4d-158">Queste coordinate interpolate sono quelle che vengono passate al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="88d4d-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="88d4d-159">I Texel non si allineano con i pixel in questo esempio; ogni pixel (e quindi ogni punto di campionamento) viene posizionato nell'angolo di quattro Texel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="88d4d-160">Poiché la modalità di filtro è impostata su lineare, il campionatore utilizzerà la media dei quattro texeli che condividono tale angolo.</span><span class="sxs-lookup"><span data-stu-id="88d4d-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="88d4d-161">In questo modo si spiega perché il pixel che dovrebbe essere rosso è in realtà costituito da tre quarti di grigio e da un quarto rosso, il pixel che dovrebbe essere verde è uno a metà grigio più uno-quarto rosso più un quarto verde e così via.</span><span class="sxs-lookup"><span data-stu-id="88d4d-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="88d4d-162">Per risolvere il problema, è sufficiente eseguire correttamente il mapping del Quad ai pixel in cui verrà eseguita la rasterizzazione, quindi eseguire correttamente il mapping dei Texel ai pixel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="88d4d-163">Nella figura seguente vengono illustrati i risultati del disegno dello stesso Quad tra (-0,5,-0,5) e (3,5, 3,5), ovvero il quad previsto dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="88d4d-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![illustrazione di un quad con trama che corrisponde al quad rasterizzato](images/maptex-fig8.png)

<span data-ttu-id="88d4d-165">Nell'illustrazione precedente viene illustrato che il quad (mostrato in (-0,5-0,5) a (3,5, 3,5)) corrisponde esattamente all'area rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="88d4d-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="88d4d-166">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="88d4d-166">Summary</span></span>

<span data-ttu-id="88d4d-167">In sintesi, i pixel e i Texel sono effettivamente punti, non blocchi solidi.</span><span class="sxs-lookup"><span data-stu-id="88d4d-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="88d4d-168">Lo spazio dello schermo ha origine in corrispondenza del pixel in alto a sinistra, ma le coordinate di trama provengono dall'angolo superiore sinistro della griglia della trama.</span><span class="sxs-lookup"><span data-stu-id="88d4d-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="88d4d-169">In particolare, ricordarsi di sottrarre 0,5 unità dai componenti x e y delle posizioni dei vertici quando si lavora nello spazio dello schermo trasformato per allineare correttamente i Texel con i pixel.</span><span class="sxs-lookup"><span data-stu-id="88d4d-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="88d4d-170">Il codice seguente è un esempio di offset dei vertici di un quadrato di 256 per 256 per visualizzare correttamente una trama 256 per 256 nello spazio dello schermo trasformato.</span><span class="sxs-lookup"><span data-stu-id="88d4d-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="88d4d-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88d4d-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88d4d-172">Coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="88d4d-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



