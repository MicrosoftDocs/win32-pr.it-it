---
description: Le risorse di trama vengono implementate nell'interfaccia IDirect3DTexture9. Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo IDirect3DDevice9::CreateTexture o una delle funzioni D3DX seguenti.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Risorse trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230caaa352a50644a6580c8aae28f18882425e40d9378cbafee1980cf317aa46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290689"
---
# <a name="texture-resources-direct3d-9"></a>Risorse trama (Direct3D 9)

Le risorse di trama vengono implementate [**nell'interfaccia IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o una delle funzioni D3DX seguenti.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

L'esempio di codice seguente [**usa D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) per caricare una trama da Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Il primo parametro accettato [**da D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) è un puntatore a [**un'interfaccia IDirect3DDevice9.**](/windows/desktop/api) Il secondo parametro indica a Direct3D il nome del file da cui caricare la trama. Il terzo parametro accetta l'indirizzo di un puntatore a [**un'interfaccia IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'oggetto trama creato.

## <a name="rendering-with-texture-resources"></a>Rendering con risorse trama

Direct3D supporta la fusione di più trame tramite il concetto di fasi della trama. Ogni fase della trama contiene una trama e operazioni che possono essere eseguite sulla trama. Le trame nelle fasi della trama formano il set di trame correnti. Per altre informazioni, vedere [Texture Blending (Direct3D 9) (Fusione delle trame (Direct3D 9).](texture-blending.md) Lo stato di ogni trama è incapsulato nella relativa fase di trama.

In un'applicazione C++ lo stato di ogni trama deve essere impostato con il [**metodo IDirect3DDevice9::SetTextureStageState.**](/windows/desktop/api) Passare il numero di fase (0-7) come valore del primo parametro. Impostare il valore del secondo parametro su un membro del [**tipo enumerato D3DTEXTURESTAGESTATETYPE.**](./d3dtexturestagestatetype.md) Il parametro finale è il valore di stato per lo stato della trama specifico.

Usando i puntatori dell'interfaccia di trama, l'applicazione può eseguire il rendering di una combinazione di un massimo di otto trame. Impostare le trame correnti richiamando il [**metodo IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Direct3D unisce tutte le trame correnti alle primitive di cui esegue il rendering.

> [!Note]  
> Il [**metodo IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa il conteggio dei riferimenti della superficie di trama assegnata. Quando la trama non è più necessaria, è necessario impostare la trama nella fase appropriata su **NULL.** Se non si riesce a eseguire questa operazione, la superficie non verrà rilasciata, causando una perdita di memoria.

 

L'applicazione può impostare lo stato di wrapping della trama per le trame correnti chiamando il [**metodo IDirect3DDevice9::SetRenderState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) Passare un valore da D3DRS WRAP0 a D3DRS WRAP7 come valore del primo parametro e usare una combinazione dei flag \_ \_ \_ D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD 2 e \_ D3DWRAPCOORD \_ 3 per abilitare il wrapping nelle direzioni u, v o w.

L'applicazione può anche impostare la prospettiva della trama e gli stati di filtro della trama. Vedere [Filtro trame (Direct3D 9).](texture-filtering.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
