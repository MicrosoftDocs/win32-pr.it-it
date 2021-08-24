---
description: Imposta i parametri di spostamento della geometria mesh.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: Metodo ID3DXPatchMesh::SetDisplaceParam (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84445c3d18fa38bbeff4085c6da1fda191bb6ca5bbe147c17f3f5f8769d2a63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629201"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a>Metodo ID3DXPatchMesh::SetDisplaceParam

Imposta i parametri di spostamento della geometria mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Trama* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Trama contenente i dati di spostamento.

</dd> <dt>

*Filtro minimo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Livello di minimità. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*MagFilter* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Livello di ingrandimento. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*Filtro mip* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Livello di filtro Mip. Per altre informazioni, vedere [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*Eseguire il wrapping* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**

Modalità di ritorno a capo dell'indirizzo della trama. Per altre informazioni, vedere [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)

</dd> <dt>

*dwLODBias* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

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

 

 
