---
description: Imposta la trasformazione sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: Metodo ID3DXSprite::SetTransform (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fba7c21d0ba0e99aefc5c4d5dfd69301bb706f804e736badcbe0227d58aca81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292618"
---
# <a name="id3dxspritesettransform-method"></a>Metodo ID3DXSprite::SetTransform

Imposta la trasformazione sprite.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTransform* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a [**un oggetto D3DXMATRIX**](d3dxmatrix.md) che contiene una trasformazione dello sprite dallo spazio mondiale originale. Usare questa trasformazione per ridimensionare, ruotare o trasformare lo sprite.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




