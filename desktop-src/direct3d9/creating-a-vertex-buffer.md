---
description: Per creare un oggetto vertex buffer, chiamare il metodo IDirect3DDevice9::CreateVertexBuffer, che accetta cinque parametri.
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Creazione di un vertex buffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c12cb50d7879ef73d4c760ac61a0698651cb9ed7d334c90475bd2e8ee4148db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527675"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Creazione di un vertex buffer (Direct3D 9)

Per creare un oggetto vertex buffer, chiamare il metodo [**IDirect3DDevice9::CreateVertexBuffer,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) che accetta cinque parametri. Il primo parametro specifica la lunghezza del buffer dei vertici, in byte. Usare l'operatore sizeof per determinare le dimensioni di un formato vertice, in byte. Si consideri il formato di vertice personalizzato seguente.


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



Per creare un vertex buffer per contenere quattro strutture CUSTOMVERTEX, specificare \[ 4 \* sizeof(CUSTOMVERTEX) \] per il parametro *Length.*

Il secondo parametro è un set di controlli di utilizzo. Tra le altre cose, il relativo valore determina se il vertex buffer è in grado di contenere informazioni di ritaglio, sotto forma di flag di ritaglio, per i vertici presenti all'esterno dell'area di visualizzazione. Per creare un vertex buffer che non può contenere flag di ritaglio, includere il flag D3DUSAGE \_ DONOTCLIP per il *parametro Usage.* Il flag DONOTCLIP D3DUSAGE viene applicato solo se si indica anche che il vertex buffer conterrà vertici trasformati. Il \_ flag D3DFVF \_ XYZRHW è incluso nel parametro *FVF.* Il metodo [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignora il flag DONOTCLIP D3DUSAGE se si indica che il buffer conterrà vertici non trasformati \_ \_ (flag XYZ D3DFVF). I flag di ritaglio occupano memoria aggiuntiva, rendendo un vertex buffer che supporta il ritaglio leggermente più grande di un buffer dei vertici non in grado di contenere flag di ritaglio. Poiché queste risorse vengono allocate al momento della creazione del vertex buffer, è necessario richiedere in anticipo un vertex buffer con supporto per il ritaglio.

Il terzo parametro, *FVF,* è una combinazione [di D3DFVF](d3dfvf.md) che descrivono il formato dei vertici del vertex buffer. Se si specifica 0 per questo parametro, il vertex buffer è un vertex buffer non FVF. Per altre informazioni, vedere [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md). Il quarto parametro descrive la classe di memoria in cui inserire il vertex buffer.

Il parametro finale accettato da [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) è l'indirizzo di una variabile che verrà riempita con un puntatore alla nuova interfaccia [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) dell'oggetto vertex buffer, se la chiamata ha esito positivo.

Non è possibile produrre flag di ritaglio per un vertex buffer creato senza supporto.

L'esempio di codice C++ seguente illustra l'aspetto della creazione di un vertex buffer nel codice.


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer dei vertici](vertex-buffers.md)
</dt> </dl>

 

 
