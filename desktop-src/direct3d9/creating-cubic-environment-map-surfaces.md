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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Creazione di superfici della mappa dell'ambiente cubico (Direct3D 9)

Si crea una trama di mappa dell'ambiente cubica chiamando il metodo [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) . Le trame della mappa dell'ambiente cubico devono essere quadrate, con dimensioni che sono una potenza di due.

Nell'esempio di codice seguente viene illustrato il modo in cui l'applicazione C++ può creare una mappa dell'ambiente cubica semplice.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Accesso ai visi Mappa dell'ambiente cubico

È possibile spostarsi tra i visi di una mappa dell'ambiente cubica usando il metodo [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .

Nell'esempio di codice riportato di seguito viene utilizzato [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) per recuperare l'area mappa del cubo utilizzata per la faccia y positiva (faccia 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Il primo parametro accettato da [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) è un valore enumerato di [**D3DCUBEMAP \_ Faces**](./d3dcubemap-faces.md) che descrive la superficie collegata che il metodo deve recuperare. Il secondo parametro indica a Direct3D il livello di una trama del cubo mipmap da recuperare. Il terzo parametro accettato è l'indirizzo dell'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , che rappresenta la superficie di trama del cubo restituita. Poiché la mappa del cubo non è mipmap, qui viene utilizzato 0.

> [!Note]
>
> Dopo la chiamata a questo metodo, il conteggio dei riferimenti interni sull'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) viene aumentato. Al termine dell'operazione, assicurarsi di chiamare il metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su questa interfaccia **IDirect3DSurface9** o si disporrà di una perdita di memoria.

 

## <a name="rendering-to-cubic-environment-maps"></a>Rendering in mappe di ambienti cubici

È possibile copiare le immagini nei singoli visi della mappa del cubo esattamente come qualsiasi altro oggetto trama o superficie. La cosa più importante da fare prima di eseguire il rendering in un viso è impostare le matrici di trasformazione in modo che la fotocamera venga posizionata correttamente e punti nella direzione corretta per quel volto: avanti (+ z), indietro (-z), a sinistra (-x), a destra (+ x), a freccia su (+ y) o giù (-y).

Nell'esempio di codice C++ riportato di seguito viene preparata e impostata una matrice di viste in base al viso sottoposto a rendering.


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



Tenere presente che ogni volto di una mappa dell'ambiente cubico rappresenta un campo di visualizzazione di 90 gradi. A meno che l'applicazione non richieda un campo di visualizzazione diverso per gli effetti speciali, ad esempio, prestare attenzione a impostare la matrice di proiezione di conseguenza.

Questo esempio di codice crea e imposta una matrice di proiezione per il caso più comune.


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



Quando la fotocamera è posizionata e la matrice di proiezione è impostata, è possibile eseguire il rendering della scena. Ogni oggetto nella scena deve essere posizionato in modo normale. L'esempio di codice seguente, fornito per completezza, descrive questa attività.


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



Si noti la chiamata al metodo [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Quando si esegue il rendering nei visi della mappa del cubo, è necessario assegnare la faccia come superficie di destinazione di rendering corrente. Le applicazioni che usano buffer di profondità possono creare in modo esplicito un buffer di profondità per la destinazione di rendering o riassegnare un buffer di profondità esistente alla superficie di destinazione di rendering. Nell'esempio di codice precedente viene usato il secondo approccio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente cubico](cubic-environment-mapping.md)
</dt> </dl>

 

 
