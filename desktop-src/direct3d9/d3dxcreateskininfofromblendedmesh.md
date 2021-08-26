---
description: Crea una mesh di interfaccia da un'altra mesh.
ms.assetid: 4c69377e-61ef-42b8-8864-c116164d4b22
title: Funzione D3DXCreateSkinInfoFromBlendedMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 77dfc11089ccedf5d435e9c15c3ec97559938d5f90506975bf15cbcdbbaa609b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952411"
---
# <a name="d3dxcreateskininfofromblendedmesh-function"></a>Funzione D3DXCreateSkinInfoFromBlendedMesh

Crea una mesh di interfaccia da un'altra mesh.

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

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a un [**oggetto ID3DXBaseMesh,**](id3dxbasemesh.md) la mesh da cui creare la mesh dell'interfaccia.

</dd> <dt>

*NumBones* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Lunghezza della matrice collegata all'elemento Disid. Vedere [**D3DXBONECOMBINATION.**](d3dxbonecombination.md)

</dd> <dt>

*pBoneCombinationTable* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXBONECOMBINATION**](d3dxbonecombination.md) \***

Puntatore a una matrice di combinazioni di combinazioni. Vedere [**D3DXBONECOMBINATION.**](d3dxbonecombination.md)

</dd> <dt>

*ppSkinInfo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXSkinInfo**](id3dxskininfo.md) che rappresenta l'oggetto mesh dell'interfaccia creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
