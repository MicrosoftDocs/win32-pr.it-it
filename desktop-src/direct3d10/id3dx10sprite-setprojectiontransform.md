---
description: Impostare la matrice di proiezione per tutti gli sprite.
ms.assetid: cb4c5546-1a31-40d9-a943-af4fbddcee01
title: Metodo ID3DX10Sprite::SetProjectionTransform (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 478fb55b500ca8e4bdc3df796ffd60ef3d9ee649e21ec1dd72b19c87a14420c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046879"
---
# <a name="id3dx10spritesetprojectiontransform-method"></a>Metodo ID3DX10Sprite::SetProjectionTransform

Impostare la matrice di proiezione per tutti gli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProjectionTransform(
  [in] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProjectionTransform* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Matrice di proiezione da usare in tutti gli sprite.

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

 

 
