---
description: Gli Stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Uso della combinazione di vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876185"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a>Uso della combinazione di vertici indicizzati (Direct3D 9)

Gli Stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit. Usare la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) per eseguire il mapping degli indici 0-255 agli Stati di trasformazione corrispondenti. Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la matrice in base al numero di stato della trasformazione 256 su una matrice di identità.


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



Per abilitare o disabilitare la fusione dei vertici indicizzati, impostare lo \_ stato di rendering INDEXEDVERTEXBLENDENABLE di D3DRS su **true**. Quando lo stato di rendering è abilitato, è necessario passare gli indici di matrice come DWORD compressi con ogni vertice. Quando questo stato di rendering è disabilitato e la fusione dei vertici è abilitata, equivale a avere gli indici di matrice 0, 1, 2 e 3 in ogni vertice. L'esempio di codice seguente usa il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) per abilitare la fusione dei vertici indicizzati.


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



Per abilitare o disabilitare la fusione dei vertici, impostare lo stato di rendering [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) su un valore diverso \_ da D3DRS Disable dal tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Se questo stato di rendering non è impostato su D3DRS \_ Disable, è necessario passare il numero necessario di pesi per ogni vertice. L'esempio di codice seguente usa **IDirect3DDevice9:: SetRenderState** per abilitare la fusione dei vertici con tre pesi per ogni vertice.


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a>Determinazione del supporto per la fusione di vertici indicizzati

Per determinare le dimensioni massime per la matrice di combinazione dei vertici indicizzati, controllare il membro MaxVertexBlendMatrixIndex della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . L'esempio di codice seguente usa il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) per recuperare questa dimensione.


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



Se il valore impostato in MaxVertexBlendMatrixIndex è 0, il dispositivo non supporta le matrici indicizzate.

> [!Note]  
> Quando si usa l'elaborazione di vertici software, è possibile usare le matrici 256 per la fusione di vertici indicizzati, con o senza la normale fusione.

 

## <a name="passing-matrix-indices-to-direct3d"></a>Passaggio di indici matrice a Direct3D

Gli indici di matrice globale possono essere passati a Direct3D usando le dichiarazioni vertex shader legacy-FVF-or.

Nell'esempio di codice seguente viene illustrato come utilizzare vertex shader legacy.


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



Quando viene usato un vertex shader legacy, gli indici di matrice vengono passati insieme alle posizioni dei vertici usando i \_ flag XYZBn di D3DFVF. Gli indici di matrice vengono passati come byte all'interno di un DWORD e devono essere presenti immediatamente dopo l'ultimo peso del vertice. Le ponderazioni del vertice vengono passate anche usando D3DFVF \_ XYZBn. Un valore DWORD compresso contiene Index3, index2, index1 e index0, dove index0 si trova nel byte più basso del valore DWORD. Il numero di indici di matrice globale usati è uguale al numero passato al numero di matrici usate per la fusione come definito da [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).

Quando viene usata una dichiarazione, D3DVSDE \_ BLENDINDICES definisce il registro dei vertici di input da cui ottenere gli indici della matrice. Gli indici della matrice devono essere passati come D3DVSDT \_ UBYTE4.

Nell'esempio di codice seguente viene illustrato come utilizzare le dichiarazioni. Si noti che l'ordine dei componenti non è più importante a meno che non si utilizzi un vertex shader a funzione fissa.

Di seguito è illustrata la dichiarazione del vertice.


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



Di seguito è illustrata la dichiarazione Register corrispondente.


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

[Unione di vertici indicizzati](indexed-vertex-blending.md)
</dt> </dl>

 

 
