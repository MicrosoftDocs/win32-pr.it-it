---
description: Ricampiona una trama nella parametrizzazione di questo gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: Metodo ID3DXTextureGutterHelper::ResampleTex (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7d3afe8155eb33a37b30abcfc96aae83c0a96461c1ee2dd6118a671701cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800320"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>Metodo ID3DXTextureGutterHelper::ResampleTex

Ricampiona una trama nella parametrizzazione di questo gutterhelper.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextureIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Trama che corrisponde alla parametrizzazione originale in pMeshIn. Questa trama verrà usata per creare pTextureOut.

</dd> <dt>

*pMeshIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh contenente le parametrizzazioni originali e nuove. È necessario archiviare la nuova parametrizzazione nell'indice D3DDECLUSAGE \_ TEXCOORD 0.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Utilizzo dei dati sui vertici (usato in combinazione con UsageIndex) che identifica il componente della dichiarazione dei vertici che contiene la parametrizzazione originale in pMeshIn. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base zero (usato in combinazione con Usage), che identifica il componente della dichiarazione dei vertici che contiene la parametrizzazione originale in pMeshIn. La combinazione di D3DDECLUSAGE TEXCOORD e indice 0 è necessaria per la nuova parametrizzazione. È possibile usare qualsiasi altra combinazione di \_ utilizzo/indice.

</dd> <dt>

*pTextureOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Trama ricampionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Una parametrizzazione nel caso di questa funzione è un set di coordinate di trama che esegue il mapping dei triangoli di una mesh ai triangoli di una trama. La nuova parametrizzazione è il set di coordinate di trama contenute nell'interfaccia helper di grondaia e la parametrizzazione originale è il set di coordinate di trama contenute nella mesh di input.

Si presuppone che le coordinate della trama siano comprese tra 0 e 1, inclusi, e che la nuova parametrizzazione deve essere dichiarata nella dichiarazione del vertice come indice delle coordinate di trama 0. La trama originale e la trama ricampionata devono avere la stessa larghezza e altezza.

Ad esempio, per preparare il ricampionamento di una trama:

-   Creare l'interfaccia di trama originale (pOriginalTex di seguito) usando una funzione come [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Creare la nuova interfaccia di trama per la trama ricampionata (pResampledTex di seguito). Le dimensioni di questa trama devono corrispondere alle dimensioni (larghezza e altezza) della trama dell'helper di grondaia.
-   Chiamare [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) per ottenere la nuova parametrizzazione, come illustrato di seguito:


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Uno scenario comune potrebbe consistere nell'usare UVAtlas per creare un at atlas di trame e quindi usare ResampleTex per ricampionare la trama nella nuova parametrizzazione. Per altre informazioni sugli atlas, vedere [Using UVAtlas (Direct3D 9) ( Uso di UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
