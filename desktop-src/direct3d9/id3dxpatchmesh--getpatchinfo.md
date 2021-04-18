---
description: Ottiene gli attributi della patch.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'Metodo ID3DXPatchMesh:: GetPatchInfo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323054"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a>Metodo ID3DXPatchMesh:: GetPatchInfo

Ottiene gli attributi della patch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PatchInfo* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**

Puntatore alle strutture contenenti gli attributi della patch. Per ulteriori informazioni sugli attributi delle patch, vedere [**D3DXPATCHINFO**](d3dxpatchinfo.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 




