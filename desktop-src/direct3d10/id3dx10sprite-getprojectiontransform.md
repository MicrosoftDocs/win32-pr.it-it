---
description: Ottiene la matrice di proiezione dello sprite applicata a tutti gli sprite.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: Metodo ID3DX10Sprite::GetProjectionTransform (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5c3f5b0a0dc60316398575855c79bdb8ac9b7113f953af75489d5b65d9ff8fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301967"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>Metodo ID3DX10Sprite::GetProjectionTransform

Ottiene la matrice di proiezione dello sprite applicata a tutti gli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProjectionTransform* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a [**un oggetto D3DX10MATRIX**](d3d10-d3dxmatrix.md) che verrà impostato sulla matrice di proiezione dello sprite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
