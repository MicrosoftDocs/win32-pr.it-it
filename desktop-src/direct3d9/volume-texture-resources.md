---
description: Le trame del volume sono raccolte tridimensionali di pixel (Texel) che possono essere usate per disegnare una primitiva bidimensionale, ad esempio un triangolo o una linea.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Risorse di trama del volume (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551424"
---
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="a8910-103">Risorse di trama del volume (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a8910-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="a8910-104">Le trame del volume sono raccolte tridimensionali di pixel (Texel) che possono essere usate per disegnare una primitiva bidimensionale, ad esempio un triangolo o una linea.</span><span class="sxs-lookup"><span data-stu-id="a8910-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="a8910-105">Le coordinate di trama a tre elementi sono obbligatorie per ogni vertice di una primitiva che deve essere tramato con un volume.</span><span class="sxs-lookup"><span data-stu-id="a8910-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="a8910-106">Quando viene disegnata la primitiva, ogni pixel contenuto viene riempito con il valore di colore di un pixel all'interno del volume, in base alle regole analoghe al caso della trama bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="a8910-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="a8910-107">Il rendering dei volumi non viene eseguito direttamente perché non sono presenti primitive tridimensionali che possono essere disegnati con loro.</span><span class="sxs-lookup"><span data-stu-id="a8910-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="a8910-108">È possibile usare le trame del volume per effetti speciali come la nebbia patch, le esplosioni e così via.</span><span class="sxs-lookup"><span data-stu-id="a8910-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="a8910-109">I volumi sono organizzati in sezioni e possono essere considerati come larghezze x altezza 2D in pila per ottenere una larghezza x altezza x volume di profondità.</span><span class="sxs-lookup"><span data-stu-id="a8910-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="a8910-110">Ogni sezione è una singola riga.</span><span class="sxs-lookup"><span data-stu-id="a8910-110">Each slice is a single row.</span></span> <span data-ttu-id="a8910-111">I volumi possono avere livelli successivi in cui le dimensioni di ogni livello vengono troncate a metà delle dimensioni del livello precedente.</span><span class="sxs-lookup"><span data-stu-id="a8910-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="a8910-112">Il diagramma seguente mostra l'aspetto di una trama del volume con più livelli.</span><span class="sxs-lookup"><span data-stu-id="a8910-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![diagramma di una trama del volume con rappresentazioni del cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="a8910-114">Creazione di una trama del volume</span><span class="sxs-lookup"><span data-stu-id="a8910-114">Creating a Volume Texture</span></span>

<span data-ttu-id="a8910-115">Negli esempi di codice riportati di seguito vengono illustrati i passaggi necessari per utilizzare una trama del volume.</span><span class="sxs-lookup"><span data-stu-id="a8910-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="a8910-116">In primo luogo, specificare un tipo di vertice personalizzato con tre coordinate di trama per ogni vertice, come illustrato in questo esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="a8910-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



<span data-ttu-id="a8910-117">Quindi, riempire i vertici con i dati.</span><span class="sxs-lookup"><span data-stu-id="a8910-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="a8910-118">A questo punto, creare un buffer vertex e riempirlo con i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="a8910-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="a8910-119">Il passaggio successivo consiste nell'usare il metodo [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) per creare una trama del volume, come illustrato in questo esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="a8910-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="a8910-120">Prima di eseguire il rendering della primitiva, impostare la trama corrente sulla trama del volume creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a8910-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="a8910-121">Nell'esempio di codice seguente viene illustrato l'intero processo di rendering per una striscia di triangoli.</span><span class="sxs-lookup"><span data-stu-id="a8910-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a><span data-ttu-id="a8910-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8910-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8910-123">Trame Direct3D</span><span class="sxs-lookup"><span data-stu-id="a8910-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
