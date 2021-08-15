---
description: Applica l'interfaccia software ai vertici di destinazione in base alle matrici correnti.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: Metodo ID3DXSkinInfo::UpdateSkinnedMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 22b36e1836570a10647f5b737a68afa1e65a4dce80fe9d49061a3eee8a799651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729453"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a>Metodo ID3DXSkinInfo::UpdateSkinnedMesh

Applica l'interfaccia software ai vertici di destinazione in base alle matrici correnti.

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

*pBoneTransforms* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice di trasformazione dell'elemento transform.

</dd> <dt>

*pBoneInvTransposeTransforms* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Trasposizione inversa della matrice di trasformazione della trasformazione inversa.

</dd> <dt>

*pVerticesSrc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer contenente i vertici di origine.

</dd> <dt>

*pVerticesDst* \[ Pollici\]
</dt> <dd>

Tipo: **[ **PVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer contenente i vertici di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Quando viene usato per eseguire l'interfaccia dei vertici con due elementi di posizione, questo metodo esegue l'interfaccia del secondo elemento di posizione con l'inverso dell'elemento anziché l'elemento stesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
