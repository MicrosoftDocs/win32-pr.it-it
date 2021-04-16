---
description: Si crea una trama di mappa dell'ambiente cubica chiamando il metodo CreateCubeTexture. Le trame della mappa dell'ambiente cubico devono essere quadrate, con dimensioni che sono una potenza di due.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Creazione di superfici della mappa dell'ambiente cubico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523834"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="01774-104">Creazione di superfici della mappa dell'ambiente cubico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="01774-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="01774-105">Si crea una trama di mappa dell'ambiente cubica chiamando il metodo [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="01774-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="01774-106">Le trame della mappa dell'ambiente cubico devono essere quadrate, con dimensioni che sono una potenza di due.</span><span class="sxs-lookup"><span data-stu-id="01774-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="01774-107">Nell'esempio di codice seguente viene illustrato il modo in cui l'applicazione C++ può creare una mappa dell'ambiente cubica semplice.</span><span class="sxs-lookup"><span data-stu-id="01774-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="01774-108">Accesso ai visi Mappa dell'ambiente cubico</span><span class="sxs-lookup"><span data-stu-id="01774-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="01774-109">È possibile spostarsi tra i visi di una mappa dell'ambiente cubica usando il metodo [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .</span><span class="sxs-lookup"><span data-stu-id="01774-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="01774-110">Nell'esempio di codice riportato di seguito viene utilizzato [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) per recuperare l'area mappa del cubo utilizzata per la faccia y positiva (faccia 2).</span><span class="sxs-lookup"><span data-stu-id="01774-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="01774-111">Il primo parametro accettato da [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) è un valore enumerato di [**D3DCUBEMAP \_ Faces**](./d3dcubemap-faces.md) che descrive la superficie collegata che il metodo deve recuperare.</span><span class="sxs-lookup"><span data-stu-id="01774-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="01774-112">Il secondo parametro indica a Direct3D il livello di una trama del cubo mipmap da recuperare.</span><span class="sxs-lookup"><span data-stu-id="01774-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="01774-113">Il terzo parametro accettato è l'indirizzo dell'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , che rappresenta la superficie di trama del cubo restituita.</span><span class="sxs-lookup"><span data-stu-id="01774-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="01774-114">Poiché la mappa del cubo non è mipmap, qui viene utilizzato 0.</span><span class="sxs-lookup"><span data-stu-id="01774-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="01774-115">Dopo la chiamata a questo metodo, il conteggio dei riferimenti interni sull'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) viene aumentato.</span><span class="sxs-lookup"><span data-stu-id="01774-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="01774-116">Al termine dell'operazione, assicurarsi di chiamare il metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su questa interfaccia **IDirect3DSurface9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="01774-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="01774-117">Rendering in mappe di ambienti cubici</span><span class="sxs-lookup"><span data-stu-id="01774-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="01774-118">È possibile copiare le immagini nei singoli visi della mappa del cubo esattamente come qualsiasi altro oggetto trama o superficie.</span><span class="sxs-lookup"><span data-stu-id="01774-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="01774-119">La cosa più importante da fare prima di eseguire il rendering in un viso è impostare le matrici di trasformazione in modo che la fotocamera venga posizionata correttamente e punti nella direzione corretta per quel volto: avanti (+ z), indietro (-z), a sinistra (-x), a destra (+ x), a freccia su (+ y) o giù (-y).</span><span class="sxs-lookup"><span data-stu-id="01774-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="01774-120">Nell'esempio di codice C++ riportato di seguito viene preparata e impostata una matrice di viste in base al viso sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="01774-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



<span data-ttu-id="01774-121">Tenere presente che ogni volto di una mappa dell'ambiente cubico rappresenta un campo di visualizzazione di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="01774-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="01774-122">A meno che l'applicazione non richieda un campo di visualizzazione diverso per gli effetti speciali, ad esempio, prestare attenzione a impostare la matrice di proiezione di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="01774-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="01774-123">Questo esempio di codice crea e imposta una matrice di proiezione per il caso più comune.</span><span class="sxs-lookup"><span data-stu-id="01774-123">This code example creates and sets a projection matrix for the most common case.</span></span>


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



<span data-ttu-id="01774-124">Quando la fotocamera è posizionata e la matrice di proiezione è impostata, è possibile eseguire il rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="01774-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="01774-125">Ogni oggetto nella scena deve essere posizionato in modo normale.</span><span class="sxs-lookup"><span data-stu-id="01774-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="01774-126">L'esempio di codice seguente, fornito per completezza, descrive questa attività.</span><span class="sxs-lookup"><span data-stu-id="01774-126">The following code example, provided for completeness, outlines this task.</span></span>


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



<span data-ttu-id="01774-127">Si noti la chiamata al metodo [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="01774-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="01774-128">Quando si esegue il rendering nei visi della mappa del cubo, è necessario assegnare la faccia come superficie di destinazione di rendering corrente.</span><span class="sxs-lookup"><span data-stu-id="01774-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="01774-129">Le applicazioni che usano buffer di profondità possono creare in modo esplicito un buffer di profondità per la destinazione di rendering o riassegnare un buffer di profondità esistente alla superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="01774-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="01774-130">Nell'esempio di codice precedente viene usato il secondo approccio.</span><span class="sxs-lookup"><span data-stu-id="01774-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01774-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01774-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01774-132">Mapping dell'ambiente cubico</span><span class="sxs-lookup"><span data-stu-id="01774-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
