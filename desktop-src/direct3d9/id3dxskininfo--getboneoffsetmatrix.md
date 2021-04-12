---
description: Ottiene la matrice di offset dell'osso.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'Metodo ID3DXSkinInfo:: GetBoneOffsetMatrix (D3DX9Mesh. h)'
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
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354094"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a>Metodo ID3DXSkinInfo:: GetBoneOffsetMatrix

Ottiene la matrice di offset dell'osso.

## <a name="syntax"></a>Sintassi


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Osso* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero osso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**

Restituisce un puntatore alla matrice di offset dell'osso. Non liberare questo puntatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[**GetNumBones**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
