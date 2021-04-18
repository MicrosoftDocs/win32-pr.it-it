---
description: Applica il skining del software ai vertici di destinazione in base alle matrici correnti.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'Metodo ID3DXSkinInfo:: UpdateSkinnedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322053"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>Metodo ID3DXSkinInfo:: UpdateSkinnedMesh

Applica il skining del software ai vertici di destinazione in base alle matrici correnti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBoneTransforms* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice di trasformazione Bone.

</dd> <dt>

*pBoneInvTransposeTransforms* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Trasponi inversa della matrice di trasformazione Bone.

</dd> <dt>

*pVerticesSrc* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer che contiene i vertici di origine.

</dd> <dt>

*pVerticesDst* \[ in\]
</dt> <dd>

Tipo: **[ **PVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer che contiene i vertici di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Quando viene usato per l'interfaccia dei vertici con due elementi position, questo metodo consente di associare il secondo elemento position con l'inverso dell'osso anziché l'osso stesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
