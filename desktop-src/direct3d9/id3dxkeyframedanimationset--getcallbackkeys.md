---
description: "Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys: riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave."
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee5a86fa5f016bd6707ec4464c79b1dc182e1ebebde80fa9f73d62e3bba3a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294987"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>Metodo ID3DXKeyframedAnimationSet::GetCallbackKeys

Riempie una matrice con i dati della chiave di callback usati per l'animazione con fotogrammi chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallbackKeys* \[ Cambio\]
</dt> <dd>

Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**

Puntatore a una matrice allocata dall'utente [**di strutture \_ CALLBACK D3DXKEY**](d3dxkey-callback.md) che il metodo deve riempire con i dati di callback.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




