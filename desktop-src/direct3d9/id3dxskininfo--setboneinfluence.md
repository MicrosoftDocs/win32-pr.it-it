---
description: Imposta il valore di influenza per un osso.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'Metodo ID3DXSkinInfo:: SetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322060"
---
# <a name="id3dxskininfosetboneinfluence-method"></a>Metodo ID3DXSkinInfo:: SetBoneInfluence

Imposta il valore di influenza per un osso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Osso* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero osso.

</dd> <dt>

*numInfluences* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di influenze.

</dd> <dt>

*vertici* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Matrice di vertici influenzato da un osso.

</dd> <dt>

*pesi* \[ in\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Matrice di pesi influenzati da un osso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
