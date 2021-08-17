---
description: Gli stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate usando indici a 8 bit.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Uso della fusione dei vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2d14e66fd934e2eaa8b403d694d203edddb229aab0795fa4a396b8baf367ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519476"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Uso della fusione dei vertici indicizzati (Direct3D 9)

Gli stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate usando indici a 8 bit. Usare la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) per eseguire il mapping degli indici da 0 a 255 agli stati di trasformazione corrispondenti. L'esempio di codice seguente illustra come usare il metodo [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la matrice in corrispondenza dello stato di trasformazione numero 256 su una matrice di identità.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Per abilitare o disabilitare la fusione dei vertici indicizzati, impostare lo stato di rendering D3DRS \_ INDEXEDVERTEXBLENDENABLE su **TRUE.** Quando lo stato di rendering è abilitato, è necessario passare gli indici della matrice come DWORD di tipo pack con ogni vertice. Quando questo stato di rendering è disabilitato e la fusione dei vertici è abilitata, equivale a avere gli indici di matrice 0, 1, 2 e 3 in ogni vertice. L'esempio di codice seguente usa il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) per abilitare la fusione dei vertici indicizzata.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Per abilitare o disabilitare la fusione dei vertici, impostare lo stato di rendering [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) su un valore diverso da D3DRS DISABLE dal tipo enumerato \_ [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Se questo stato di rendering non è impostato su D3DRS DISABLE, è necessario passare il numero richiesto di pesi \_ per ogni vertice. L'esempio di codice seguente usa **IDirect3DDevice9::SetRenderState** per abilitare la fusione dei vertici con tre pesi per ogni vertice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinazione del supporto della fusione dei vertici indicizzati

Per determinare le dimensioni massime per la matrice di fusione dei vertici indicizzati, controllare il membro MaxVertexBlendMatrixIndex della struttura [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) L'esempio di codice seguente usa il [**metodo IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) per recuperare queste dimensioni.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Se il valore impostato in MaxVertexBlendMatrixIndex è 0, il dispositivo non supporta le matrici indicizzate.

> [!Note]  
> Quando si usa l'elaborazione dei vertici software, è possibile usare 256 matrici per la fusione dei vertici indicizzata, con o senza la normale fusione.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Passaggio di indici di matrice a Direct3D

Gli indici della matrice globale possono essere passati a Direct3D usando vertex shader legacy - FVF - o dichiarazioni.

L'esempio di codice seguente illustra come usare vertex shader legacy.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



Quando si usa un vertex shader legacy, gli indici di matrice vengono passati insieme alle posizioni dei vertici usando i flag D3DFVF \_ XYZBn. Gli indici di matrice vengono passati come byte all'interno di un valore DWORD e devono essere presenti immediatamente dopo l'ultimo peso del vertice. I pesi dei vertici vengono passati anche usando D3DFVF \_ XYZBn. Un valore DWORD pack contiene index3, index2, index1 e index0, dove index0 si trova nel byte più basso della DWORD. Il numero di indici world-matrix usati è uguale al numero passato al numero di matrici usate per la fusione, come definito da [**\_ VERTEXBLEND D3DRS.**](./d3drenderstatetype.md)

Quando si usa una dichiarazione, D3DVSDE BLENDINDICES definisce il registro vertici di input da cui \_ ottenere gli indici della matrice. Gli indici di matrice devono essere passati come \_ UBYTE4 D3DVSDT.

L'esempio di codice seguente illustra come usare le dichiarazioni. Si noti che l'ordine dei componenti non è più importante a meno che non si utilizzi un vertex shader a funzione fissa.

Ecco la dichiarazione dei vertici.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Ecco la dichiarazione di registro corrispondente.


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione di vertici indicizzati](indexed-vertex-blending.md)
</dt> </dl>

 

 
