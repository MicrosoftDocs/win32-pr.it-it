---
description: Ricampiona una trama nella parametrizzazione di questo gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'Metodo ID3DXTextureGutterHelper:: ResampleTex (D3DX9Mesh. h)'
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
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235136"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>Metodo ID3DXTextureGutterHelper:: ResampleTex

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

*pTextureIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Trama che corrisponde alla parametrizzazione originale in pMeshIn. Questa trama verrà usata per creare pTextureOut.

</dd> <dt>

*pMeshIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh contenente le parametrizzazioni originali e nuove. È necessario archiviare la nuova parametrizzazione in D3DDECLUSAGE \_ TEXCOORD index 0.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Utilizzo dei dati dei vertici (usato in combinazione con UsageIndex) che identifica il componente della dichiarazione di vertice che contiene la parametrizzazione originale in pMeshIn. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice in base zero (usato in combinazione con Usage), che identifica il componente della dichiarazione di vertice che contiene la parametrizzazione originale in pMeshIn. \_Per la nuova parametrizzazione è necessaria la combinazione di D3DDECLUSAGE TEXCOORD e index 0. qualsiasi altra combinazione di utilizzo/indice può essere utilizzata.

</dd> <dt>

*pTextureOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Trama ricampionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Una parametrizzazione nel caso di questa funzione è un set di coordinate di trama che esegue il mapping dei triangoli di una mesh ai triangoli di una trama. La nuova parametrizzazione è il set di coordinate di trama contenute nell'interfaccia di supporto della barra di navigazione e la parametrizzazione originale è il set di coordinate di trama contenute all'interno della mesh di input.

Si presuppone che le coordinate di trama siano comprese tra 0 e 1, inclusi, e la nuova parametrizzazione deve essere dichiarata nella dichiarazione del vertice come coordinata di trama indice 0. La trama originale e la trama ricampionata devono avere la stessa larghezza e altezza.

Ad esempio, per preparare il ricampionamento di una trama:

-   Creare l'interfaccia di trama originale (pOriginalTex sotto) usando una funzione come [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).
-   Creare la nuova interfaccia di trama per la trama ricampionata (pResampledTex di seguito). Le dimensioni di questa trama devono corrispondere alla dimensione (larghezza e altezza) della trama di supporto della barra di navigazione.
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



Uno scenario comune potrebbe consistere nell'usare UVAtlas per creare un Atlante di trama e quindi usare ResampleTex per ricampionare la trama nella nuova parametrizzazione. Per altre informazioni sugli atlanti, vedere [uso di UVAtlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
