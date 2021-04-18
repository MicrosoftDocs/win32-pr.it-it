---
description: Imposta un valore di influenza di un osso in un singolo vertice.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'Metodo ID3DXSkinInfo:: SetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322052"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a>Metodo ID3DXSkinInfo:: SetBoneVertexInfluence

Imposta un valore di influenza di un osso in un singolo vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*boneNum* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice dell'osso. Deve essere compreso tra 0 e il numero di ossa.

</dd> <dt>

*influenceNum* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice della matrice di influenza dell'osso specificato.

</dd> <dt>

*peso* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fattore di fusione dell'influenza dell'osso specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
