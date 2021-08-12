---
description: 'Metodo ID3DXKeyframedAnimationSet::GetCallbackKey: ottiene informazioni su un callback specifico nel set di animazioni.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: Metodo ID3DXKeyframedAnimationSet::GetCallbackKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5036ca9e00da3231677fe41e179bb9c27d1a4bbbd145f3e15bc6e4160902e9b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295171"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>Metodo ID3DXKeyframedAnimationSet::GetCallbackKey

Ottiene informazioni su un callback specifico nel set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice dell'animazione.

</dd> <dt>

*pCallbackKeys* \[ Cambio\]
</dt> <dd>

Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**

Puntatore alla [**funzione di callback**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
