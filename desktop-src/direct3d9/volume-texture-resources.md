---
description: Le trame di volume sono raccolte tridimensionali di pixel (texel) che possono essere usate per disegnare una primitiva bidimensionale, ad esempio un triangolo o una linea.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Risorse trame di volume (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e72448fd1fd4856cf81a344f5c176fdb6272546468126975edbff8b20218d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984357"
---
# <a name="volume-texture-resources-direct3d-9"></a>Risorse trame di volume (Direct3D 9)

Le trame di volume sono raccolte tridimensionali di pixel (texel) che possono essere usate per disegnare una primitiva bidimensionale, ad esempio un triangolo o una linea. Le coordinate di trama a tre elementi sono necessarie per ogni vertice di una primitiva che deve essere strutturata con un volume. Quando viene disegnata la primitiva, ogni pixel contenuto viene riempito con il valore del colore di un pixel all'interno del volume, in base a regole analoghe alla combinazione di maiuscole e minuscole della trama bidimensionale. Il rendering dei volumi non viene eseguito direttamente perché non è possibile disegnare primitive tridimensionali.

È possibile usare trame di volume per effetti speciali, ad esempio nebbia patchy, esplosioni e così via.

I volumi sono organizzati in sezioni e possono essere pensati come superfici 2D in larghezza x altezza impilati per creare un volume di larghezza x altezza x profondità. Ogni sezione è una singola riga. I volumi possono avere livelli successivi in cui le dimensioni di ogni livello vengono troncate a metà delle dimensioni del livello precedente. Il diagramma seguente illustra l'aspetto di una trama di volume con più livelli.

![diagramma di una trama di volume con rappresentazioni di cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Creazione di una trama del volume

Gli esempi di codice seguenti illustrano i passaggi necessari per usare una trama del volume.

Specificare innanzitutto un tipo di vertice personalizzato con tre coordinate di trama per ogni vertice, come illustrato in questo esempio di codice.


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



Quindi, riempire i vertici con i dati.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



Creare ora un vertex buffer e riempirlo con i dati dei vertici.

Il passaggio successivo consiste nell'usare il metodo [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) per creare una trama del volume, come illustrato in questo esempio di codice.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Prima di eseguire il rendering della primitiva, impostare la trama corrente sulla trama del volume creata in precedenza. L'esempio di codice seguente illustra l'intero processo di rendering per una striscia di triangoli.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
