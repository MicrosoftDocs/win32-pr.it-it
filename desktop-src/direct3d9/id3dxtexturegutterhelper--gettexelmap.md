---
description: Recupera le coordinate di trama (u, v) di ogni texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: Metodo ID3DXTextureGutterHelper::GetTexelMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 321f5075bdfde3a5a3d707089867356b3f702230dd81d2a1c29b513a8cf8e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800374"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>Metodo ID3DXTextureGutterHelper::GetTexelMap

Recupera le coordinate di trama (u, v) di ogni texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTexelData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntatore alla posizione in coordinate di trama in pixel (u, v) in cui si trova ogni texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

Per le classi 2 e [**4 texel,**](id3dxtexturegutterhelper.md)le coordinate di trama restituite (u, v) corrispondono al punto più vicino sul triangolo più vicino.

L'applicazione deve allocare e gestire pTexelData.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




