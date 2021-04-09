---
description: Ottiene le dimensioni della mesh tassellati, dato un livello a mosaico.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'Metodo ID3DXPatchMesh:: GetTessSize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef23f46baca7e05005cee83f6ca765b9a5214b8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058696"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>Metodo ID3DXPatchMesh:: GetTessSize

Ottiene le dimensioni della mesh tassellati, dato un livello a mosaico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTessLevel* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Livello mosaico.

</dd> <dt>

*Adattivo* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Mosaico adattivo. Per lo schema a mosaico adattivo, impostare questo valore su **true** e impostare fTessLevel sul valore massimo a mosaico. Ciò comporterà la dimensione massima della mesh necessaria per lo schema a mosaico adattivo.

</dd> <dt>

*NumTriangles* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di triangoli generati dalla mesh tassellati.

</dd> <dt>

*NumVertices* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di vertici generati dalla mesh tassellati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo presuppone un mosaico uniforme.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
