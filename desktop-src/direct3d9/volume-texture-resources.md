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
# <a name="volume-texture-resources-direct3d-9"></a>Risorse di trama del volume (Direct3D 9)

Le trame del volume sono raccolte tridimensionali di pixel (Texel) che possono essere usate per disegnare una primitiva bidimensionale, ad esempio un triangolo o una linea. Le coordinate di trama a tre elementi sono obbligatorie per ogni vertice di una primitiva che deve essere tramato con un volume. Quando viene disegnata la primitiva, ogni pixel contenuto viene riempito con il valore di colore di un pixel all'interno del volume, in base alle regole analoghe al caso della trama bidimensionale. Il rendering dei volumi non viene eseguito direttamente perché non sono presenti primitive tridimensionali che possono essere disegnati con loro.

È possibile usare le trame del volume per effetti speciali come la nebbia patch, le esplosioni e così via.

I volumi sono organizzati in sezioni e possono essere considerati come larghezze x altezza 2D in pila per ottenere una larghezza x altezza x volume di profondità. Ogni sezione è una singola riga. I volumi possono avere livelli successivi in cui le dimensioni di ogni livello vengono troncate a metà delle dimensioni del livello precedente. Il diagramma seguente mostra l'aspetto di una trama del volume con più livelli.

![diagramma di una trama del volume con rappresentazioni del cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Creazione di una trama del volume

Negli esempi di codice riportati di seguito vengono illustrati i passaggi necessari per utilizzare una trama del volume.

In primo luogo, specificare un tipo di vertice personalizzato con tre coordinate di trama per ogni vertice, come illustrato in questo esempio di codice.


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



A questo punto, creare un buffer vertex e riempirlo con i dati dei vertici.

Il passaggio successivo consiste nell'usare il metodo [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) per creare una trama del volume, come illustrato in questo esempio di codice.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Prima di eseguire il rendering della primitiva, impostare la trama corrente sulla trama del volume creata in precedenza. Nell'esempio di codice seguente viene illustrato l'intero processo di rendering per una striscia di triangoli.


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

 

 
