---
description: Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'Metodo ID3DXSkinInfo:: GetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354074"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a>Metodo ID3DXSkinInfo:: GetBoneVertexInfluence

Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
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

*pWeight* \[ in uscita\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore al fattore di Blend influenzato da influenceNum.

</dd> <dt>

*pVertexNum* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al vertice influenzato da influenceNum.

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

[**ID3DXSkinInfo::SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
