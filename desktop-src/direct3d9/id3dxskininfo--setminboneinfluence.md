---
description: Imposta l'influenza minima del colore. I valori di influenza inferiori a questo valore vengono ignorati.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: Metodo ID3DXSkinInfo::SetMinBoneInfluence (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: abe9f1d7f9c54b9c3086160b974e2bc7dc659eb6dae3ff647f059627ff3ef145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747481"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a>Metodo ID3DXSkinInfo::SetMinBoneInfluence

Imposta l'influenza minima del colore. I valori di influenza inferiori a questo valore vengono ignorati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MinInfl* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore minimo di influenza. I valori di influenza inferiori a questo valore vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
