---
description: Crea una mesh di interfaccia personalizzata da un'altra mesh.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Funzione D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFromBlendedMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d81de43dde2b4f0df5913831ddfcefbab1a41855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530925"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>D3DXCreateSkinInfoFromBlendedMesh (funzione)

Crea una mesh di interfaccia personalizzata da un'altra mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateSkinInfoFromBlendedMesh(
  _In_        LPD3DXBASEMESH      pMesh,
  _In_        DWORD               NumBones,
  _In_  const D3DXBONECOMBINATION *pBoneCombinationTable,
  _Out_       LPD3DXSKININFO      *ppSkinInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a un oggetto [**ID3DXBaseMesh**](id3dxbasemesh.md) , mesh da cui creare la mesh dell'interfaccia.

</dd> <dt>

*NumBones* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Lunghezza della matrice associata a BoneId. Vedere [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*pBoneCombinationTable* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Puntatore a una matrice di combinazioni di osso. Vedere [**D3DXBONECOMBINATION**](d3dxbonecombination.md).

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXSkinInfo**](id3dxskininfo.md) che rappresenta l'oggetto mesh interfaccia creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
