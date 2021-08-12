---
description: Ottenere informazioni sulla traduzione per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: Metodo ID3DXKeyframedAnimationSet::GetTranslationKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b09eac144382bb21114b1c9b3b878baca57fb134555e37bea00580a9f2bfba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294942"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a>Metodo ID3DXKeyframedAnimationSet::GetTranslationKey

Ottenere informazioni sulla traduzione per un fotogramma chiave specifico nel set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
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

*pTranslationKey* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntatore alle informazioni sulla rotazione. Vedere [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

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

 

 
