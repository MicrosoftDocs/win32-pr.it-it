---
description: Ottiene i vertici e i pesi influenzati da un osso.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'Metodo ID3DXSkinInfo:: GetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322066"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>Metodo ID3DXSkinInfo:: GetBoneInfluence

Ottiene i vertici e i pesi influenzati da un osso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Osso* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero osso.

</dd> <dt>

*vertici* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ottenere la matrice di vertici influenzato da un osso.

</dd> <dt>

*pesi* \[ in uscita\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ottenere la matrice di pesi influenzata da un osso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Usare [**ID3DXSkinInfo:: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) per determinare il numero di vertici influenzati dall'osso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
