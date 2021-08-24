---
description: Per creare una trama della mappa dell'ambiente cubico, chiamare il metodo CreateCubeTexture. Le trame delle mappe dell'ambiente cubico devono essere quadrate, con dimensioni che sono una potenza di due.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Creazione di superfici mappa dell'ambiente cubico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b37321978a40170d47718318e4b3f6898ba04d5fa229e97ada47e08e589fdcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608021"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Creazione di superfici mappa dell'ambiente cubico (Direct3D 9)

Per creare una trama della mappa dell'ambiente cubico, chiamare il [**metodo CreateCubeTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) Le trame delle mappe dell'ambiente cubico devono essere quadrate, con dimensioni che sono una potenza di due.

L'esempio di codice seguente illustra come l'applicazione C++ potrebbe creare una semplice mappa dell'ambiente cubico.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Accesso ai visi della mappa dell'ambiente cubico

È possibile spostarsi tra i visi di una mappa dell'ambiente cubico usando il [**metodo GetCubeMapSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)

L'esempio di codice seguente usa [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) per recuperare la superficie della mappa del cubo usata per la faccia y positiva (viso 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Il primo parametro accettato da [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) è un valore enumerato [**FACES D3DCUBEMAP \_**](./d3dcubemap-faces.md) che descrive la superficie associata che il metodo deve recuperare. Il secondo parametro indica a Direct3D quale livello di trama del cubo mipmapped recuperare. Il terzo parametro accettato è l'indirizzo [**dell'interfaccia IDirect3DSurface9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) che rappresenta la superficie di trama del cubo restituita. Poiché questa mappa del cubo non è mipmapped, in questo caso viene usato 0.

> [!Note]
>
> Dopo la chiamata a questo metodo, il conteggio dei riferimenti interni [**sull'interfaccia IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) viene aumentato. Al termine dell'uso di questa superficie, assicurarsi di chiamare il metodo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su questa **interfaccia IDirect3DSurface9** oppure si avrà una perdita di memoria.

 

## <a name="rendering-to-cubic-environment-maps"></a>Rendering nell'ambiente cubico Mappe

È possibile copiare le immagini nei singoli visi della mappa del cubo esattamente come qualsiasi altro oggetto trama o superficie. La cosa più importante da fare prima del rendering su un viso è impostare le matrici di trasformazione in modo che la fotocamera sia posizionata correttamente e punti nella direzione appropriata per tale viso: avanti (+z), indietro (-z), sinistra (-x), destra (+x), su (+y) o giù (-y).

L'esempio di codice C++ seguente prepara e imposta una matrice di visualizzazione in base al viso sottoposto a rendering.


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



Tenere presente che ogni viso di una mappa dell'ambiente cubico rappresenta un campo di visualizzazione a 90 gradi. A meno che l'applicazione non richieda un angolo di visualizzazione diverso, ad esempio per gli effetti speciali, è necessario impostare la matrice di proiezione di conseguenza.

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



Quando la fotocamera è in posizione e la matrice di proiezione è impostata, è possibile eseguire il rendering della scena. Ogni oggetto nella scena deve essere posizionato come si farebbe normalmente. L'esempio di codice seguente, fornito per completezza, descrive questa attività.


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



Si noti la chiamata al [**metodo SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) Quando si esegue il rendering dei visi della mappa del cubo, è necessario assegnare il viso come superficie di destinazione di rendering corrente. Le applicazioni che usano buffer di profondità possono creare in modo esplicito un buffer di profondità per la destinazione di rendering o riassegnare un buffer di profondità esistente alla superficie di destinazione del rendering. L'esempio di codice precedente usa il secondo approccio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping dell'ambiente cubico](cubic-environment-mapping.md)
</dt> </dl>

 

 
