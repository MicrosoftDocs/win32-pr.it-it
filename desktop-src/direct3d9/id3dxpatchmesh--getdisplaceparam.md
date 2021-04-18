---
description: Ottiene i parametri di spostamento della geometria mesh.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'Metodo ID3DXPatchMesh:: GetDisplaceParam (D3DX9Mesh. h)'
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
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323721"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>Metodo ID3DXPatchMesh:: GetDisplaceParam

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

*Trama* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Trama contenente i dati di spostamento.

</dd> <dt>

*MinFilter* \[ in\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello minification. Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ in\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello di ingrandimento. Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Livello di filtro MIP. Per ulteriori informazioni, vedere [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

A *capo automatico* \[ in\]
</dt> <dd>

Tipo: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Modalità di wrapping degli indirizzi della trama. Per ulteriori informazioni, vedere [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*dwLODBias* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Livello del valore di distorsione del dettaglio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Le mappe di spostamento possono essere solo trame 2D. Mapping MIP viene ignorato per lo schema a mosaico non adattivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
