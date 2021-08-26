---
description: L'applicazione modifica le risorse per eseguire il rendering di una scena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipolazione delle risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0a9cf2ee85b2f8e86077eb525acffb914e60cba84082c9d610e10da9f5fa02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069051"
---
# <a name="manipulating-resources-direct3d-9"></a>Manipolazione delle risorse (Direct3D 9)

L'applicazione modifica le risorse per eseguire il rendering di una scena. In primo luogo, un'applicazione deve creare una risorsa trama con uno dei metodi seguenti:

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

È invece possibile creare una risorsa trama con una delle funzioni di texturing D3DXCreatexxx.

Gli oggetti trama restituiti dai metodi di creazione della trama sono contenitori per superfici o volumi. Questi contenitori sono genericamente noti come buffer. I buffer di proprietà della risorsa ereditano gli utilizzi, il formato e il pool della risorsa, ma hanno il proprio tipo. Per altre informazioni, vedere [Proprietà risorsa (Direct3D 9).](resource-properties.md)

L'applicazione ottiene l'accesso alle superfici contenute, allo scopo di caricare grafica, chiamando i metodi seguenti. Per informazioni dettagliate, [vedere Blocco delle risorse (Direct3D 9).](locking-resources.md)

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

I metodi lock accettano argomenti che denotano la superficie contenuta, ad esempio la faccia del cubo o del sotto livello mipmap della trama, e restituiscono puntatori ai pixel. L'applicazione tipica non usa mai direttamente un oggetto surface.

Creare risorse orientate alla geometria chiamando [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) o [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Bloccare e riempire le risorse del buffer chiamando [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) o [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), a seconda della risorsa.

Per le risorse di trama gestite, il processo di creazione delle risorse termina qui. Per le risorse di trama non gestite, un'applicazione promuove le risorse della memoria di sistema a risorse accessibili dal dispositivo (per l'accelerazione hardware) chiamando [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Per presentare le immagini di cui viene eseguito il rendering dalle risorse, l'applicazione necessita anche di buffer di colori e stencil di profondità. Per le applicazioni tipiche, il buffer dei colori è di proprietà della catena di scambio del dispositivo, che è una raccolta di superfici del buffer nascosto e viene creato in modo implicito con il dispositivo. Le superfici depth-stencil possono essere create in modo implicito o in modo esplicito usando il metodo [**IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/desktop/api) L'applicazione associa un dispositivo e il relativo buffer di profondità e colore a una chiamata a [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) o [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Per informazioni dettagliate sulla presentazione dell'immagine finale, vedere [Presentazione di una scena (Direct3D 9).](presenting-a-scene.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
