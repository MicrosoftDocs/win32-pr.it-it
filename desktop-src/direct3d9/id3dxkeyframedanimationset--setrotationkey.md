---
description: Impostare le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: b31edc88-0d77-49f3-b4c4-39cd866e1379
title: Metodo ID3DXKeyframedAnimationSet::SetRotationKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2375167b9c848c0ccec10853f04c2f1aa7b59992d3198164df46c0ba7c08b68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856601"
---
# <a name="id3dxkeyframedanimationsetsetrotationkey-method"></a>Metodo ID3DXKeyframedAnimationSet::SetRotationKey

Impostare le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice dell'animazione.

</dd> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Fotogramma chiave.

</dd> <dt>

*pRotationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**

Puntatore ai dati di rotazione. Vedere [**D3DXKEY \_ VECTOR3.**](d3dxkey-vector3.md)

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

 

 
