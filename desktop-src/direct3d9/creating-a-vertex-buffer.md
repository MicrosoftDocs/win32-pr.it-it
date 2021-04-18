---
description: 'Si crea un oggetto vertex buffer chiamando il metodo IDirect3DDevice9:: CreateVertexBuffer, che accetta cinque parametri.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Creazione di un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305188"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Creazione di un buffer vertex (Direct3D 9)

Si crea un oggetto vertex buffer chiamando il metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , che accetta cinque parametri. Il primo parametro specifica la lunghezza in byte del buffer del vertice. Usare l'operatore sizeof per determinare le dimensioni in byte del formato del vertice. Si consideri il seguente formato di vertice personalizzato.


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



Per creare un buffer vertex per mantenere quattro strutture CUSTOMVERTEX, specificare \[ 4 \* sizeof (CUSTOMVERTEX) \] per il parametro *length* .

Il secondo parametro è un set di controlli di utilizzo. Tra le altre cose, il valore determina se il buffer dei vertici è in grado di contenere informazioni di ritaglio, sotto forma di flag di ritaglio, per i vertici presenti all'esterno dell'area di visualizzazione. Per creare un buffer vertex che non può contenere i flag di ritaglio, includere il \_ flag D3DUSAGE DONOTCLIP per il parametro *Usage* . Il \_ flag DONOTCLIP di D3DUSAGE viene applicato solo se si indica anche che il buffer dei vertici conterrà i vertici trasformati \_ . il flag XYZRHW di D3DFVF è incluso nel parametro *FVF* . Il metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignora il \_ flag DONOTCLIP di D3DUSAGE se si indica che il buffer conterrà i vertici non trasformati (il \_ flag D3DFVF XYZ). I flag di ritaglio occupano memoria aggiuntiva, rendendo leggermente più grande un buffer di vertici con supporto per il ritaglio rispetto a un buffer di vertex che non supporta i flag di ritaglio. Poiché queste risorse vengono allocate quando viene creato il buffer dei vertici, è necessario richiedere in anticipo un buffer dei vertici con supporto di ritaglio.

Il terzo parametro, *FVF*, è una combinazione di [D3DFVF](d3dfvf.md) che descrivono il formato dei vertici del buffer del vertice. Se si specifica 0 per questo parametro, il buffer dei vertici è un vertex buffer non FVF. Per altre informazioni, vedere [FVF vertex buffers (Direct3D 9)](fvf-vertex-buffers.md). Il quarto parametro descrive la classe di memoria in cui posizionare il buffer dei vertici.

Il parametro finale che [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accetta è l'indirizzo di una variabile che verrà compilata con un puntatore alla nuova interfaccia [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) dell'oggetto vertex buffer, se la chiamata ha esito positivo.

Non è possibile produrre i flag di ritaglio per un buffer di vertex creato senza supporto.

Nell'esempio di codice C++ riportato di seguito viene illustrato l'aspetto della creazione di un buffer vertex nel codice.


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

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 
