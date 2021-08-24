---
description: Ottiene la matrice di offset dell'osso.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: Metodo ID3DXSkinInfo::GetBoneOffsetMatrix (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d10586fc9d4008ebd22b7edf2fa955628ffa0ab703ef70ed06cb2f2cb1fd8d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492301"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>Metodo ID3DXSkinInfo::GetBoneOffsetMatrix

Ottiene la matrice di offset dell'osso.

## <a name="syntax"></a>Sintassi


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Osso* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di osso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Restituisce un puntatore alla matrice di offset dell'osso. Non liberare questo puntatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
