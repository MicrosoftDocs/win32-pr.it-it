---
description: Imposta l'indice della faccia mesh a cui appartiene ogni texel.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: Metodo ID3DXTextureGutterHelper::SetFaceMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7de812f5445d0d8d704aeba939cf8cbc4441d4ed542bf716371a7fc12a1ba6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747381"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>Metodo ID3DXTextureGutterHelper::SetFaceMap

Imposta l'indice della faccia mesh a cui appartiene ogni texel.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFaceData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore all'indice della faccia mesh a cui appartiene ogni texel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'input dei dati del viso mesh per questo metodo è valido solo per texel validi (non di classe 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i texel validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
