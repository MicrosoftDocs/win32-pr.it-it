---
description: Ottiene la trasformazione di visualizzazione che si applica a tutti gli sprite.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: Metodo ID3DX10Sprite::GetViewTransform (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 664cded793fff7b37c7d1218d8d87d50cc0bc57ac290a4bba07bff0cdf169050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736029"
---
# <a name="id3dx10spritegetviewtransform-method"></a>Metodo ID3DX10Sprite::GetViewTransform

Ottiene la trasformazione di visualizzazione che si applica a tutti gli sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pViewTransform* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntatore a [**un oggetto D3DX10MATRIX**](d3d10-d3dxmatrix.md) che verrà impostato sulla trasformazione dello sprite dallo spazio mondiale originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

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

 

 
