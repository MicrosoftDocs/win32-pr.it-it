---
description: L'applicazione modifica le risorse per eseguire il rendering di una scena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipolazione di risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401041"
---
# <a name="manipulating-resources-direct3d-9"></a>Manipolazione di risorse (Direct3D 9)

L'applicazione modifica le risorse per eseguire il rendering di una scena. Per prima cosa, un'applicazione deve creare una risorsa di trama con uno dei metodi seguenti:

-   [**IDirect3DDevice9:: CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

È invece possibile creare una risorsa di trama con una delle funzioni di texturing di D3DXCreatexxx.

Gli oggetti trama restituiti dai metodi di creazione della trama sono contenitori per superfici o volumi; questi contenitori sono noti in modo generico come buffer. I buffer di proprietà della risorsa ereditano gli utilizzi, il formato e il pool della risorsa, ma hanno un proprio tipo. Per altre informazioni, vedere [proprietà delle risorse (Direct3D 9)](resource-properties.md).

L'applicazione ottiene l'accesso alle superfici contenute, allo scopo di caricare le illustrazioni, chiamando i metodi seguenti. Per informazioni dettagliate, vedere [blocco di risorse (Direct3D 9)](locking-resources.md).

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9:: archivio protetto**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

I metodi di blocco accettano argomenti che indicano la superficie contenuta, ad esempio il sottolivello o il lato del cubo mipmap della trama, e restituiscono puntatori ai pixel. L'applicazione tipica non utilizza mai direttamente un oggetto Surface.

Creare risorse orientate alla geometria chiamando [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/desktop/api) o [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Bloccare e riempire le risorse del buffer chiamando [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) o [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), a seconda della risorsa.

Per le risorse di trama gestite, il processo di creazione delle risorse termina qui. Per le risorse di trama non gestite, un'applicazione promuove le risorse di memoria di sistema a risorse accessibili dal dispositivo (per l'accelerazione hardware) chiamando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Per presentare le immagini sottoposte a rendering dalle risorse, l'applicazione necessita anche di buffer di colore e di stencil di profondità. Per le applicazioni tipiche, il buffer dei colori appartiene alla catena di scambio del dispositivo, che è una raccolta di superfici di back-buffer e viene creata in modo implicito con il dispositivo. Le superfici dello stencil Depth possono essere create in modo implicito o create in modo esplicito tramite il metodo [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/desktop/api) . L'applicazione associa un dispositivo e il relativo buffer di profondità e colore con una chiamata a [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) o [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Per informazioni dettagliate sulla presentazione dell'immagine finale, vedere [presentazione di una scena (Direct3D 9)](presenting-a-scene.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
