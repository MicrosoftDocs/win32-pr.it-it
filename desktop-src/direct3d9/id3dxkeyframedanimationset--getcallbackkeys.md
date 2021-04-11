---
description: Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Metodo ID3DXKeyframedAnimationSet:: GetCallbackKeys (D3dx9anim. h)'
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
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234961"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>Metodo ID3DXKeyframedAnimationSet:: GetCallbackKeys

Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCallbackKeys* \[ out\]
</dt> <dd>

Tipo: **[ **\_ callback LPD3DXKEY**](d3dxkey-callback.md)**

Puntatore a una matrice allocata dall'utente di strutture di [**\_ callback D3DXKEY**](d3dxkey-callback.md) che il metodo deve compilare con i dati di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




