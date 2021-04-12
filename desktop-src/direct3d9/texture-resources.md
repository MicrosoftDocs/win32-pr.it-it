---
description: "Le risorse di trama sono implementate nell'interfaccia IDirect3DTexture9. Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo IDirect3DDevice9:: CreateTexture o una delle funzioni D3DX seguenti."
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Risorse di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225469"
---
# <a name="texture-resources-direct3d-9"></a>Risorse di trama (Direct3D 9)

Le risorse di trama sono implementate nell'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) . Per ottenere un puntatore a un'interfaccia di trama, chiamare il metodo [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o una delle funzioni D3DX seguenti.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

Nell'esempio di codice seguente viene usato [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) per caricare una trama da Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



Il primo parametro accettato da [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) è un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) . Il secondo parametro indica a Direct3D il nome del file da cui caricare la trama. Il terzo parametro accetta l'indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.

## <a name="rendering-with-texture-resources"></a>Rendering con risorse di trama

Direct3D supporta la fusione di più trame attraverso il concetto di fasi della trama. Ogni fase della trama contiene una trama e le operazioni che possono essere eseguite sulla trama. Le trame nelle fasi della trama formano il set di trame correnti. Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md). Lo stato di ogni trama viene incapsulato nella fase della trama.

In un'applicazione C++ lo stato di ogni trama deve essere impostato con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) . Passare il numero di fase (0-7) come valore del primo parametro. Impostare il valore del secondo parametro su un membro del tipo enumerato [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . Il parametro finale è il valore dello stato per lo stato della trama particolare.

Usando i puntatori dell'interfaccia di trama, l'applicazione può eseguire il rendering di una blend di un massimo di otto trame. Impostare le trame correnti richiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Direct3D combina tutte le trame correnti sulle primitive di cui esegue il rendering.

> [!Note]  
> Il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa il conteggio dei riferimenti della superficie della trama da assegnare. Quando la trama non è più necessaria, è necessario impostare la trama nella fase appropriata su **null**. Se non si riesce a eseguire questa operazione, la superficie non verrà rilasciata, causando una perdita di memoria.

 

L'applicazione può impostare lo stato di wrapping della trama per le trame correnti chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . Passare un valore da D3DRS \_ WRAP0 a D3DRS \_ WRAP7 come valore del primo parametro e usare una combinazione dei \_ flag D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 e D3DWRAPCOORD \_ 3 per abilitare il ritorno a capo nelle direzioni u, v o w.

L'applicazione può anche impostare la prospettiva della trama e gli Stati di filtro della trama. Vedere [filtro delle trame (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
