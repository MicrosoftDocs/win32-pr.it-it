---
description: Ottiene i parametri di spostamento della geometria mesh.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: Metodo ID3DXPatchMesh::GetDisplaceParam (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f079e66f20bfd9b2fab673a0f8c2310a9fd85d84fe4e7d0b8c5ad59d1d61e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847451"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>Metodo ID3DXPatchMesh::GetDisplaceParam

Ottiene i parametri di spostamento della geometria mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Trama* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Trama contenente i dati di spostamento.

</dd> <dt>

*Filtro minimo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello di minimità. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*MagFilter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello di ingrandimento. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*Filtro mip* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello di filtro Mip. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*Eseguire il wrapping* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Modalità di ritorno a capo dell'indirizzo della trama. Per altre informazioni, vedere [**D3DTEXTUREADDRESS.**](./d3dtextureaddress.md)

</dd> <dt>

*dwLODBias* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Valore di distorsione del livello di dettaglio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Le mappe di spostamento possono essere solo trame 2D. L'applicazione mipm viene ignorata per lo schema a tessitura non adatta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
