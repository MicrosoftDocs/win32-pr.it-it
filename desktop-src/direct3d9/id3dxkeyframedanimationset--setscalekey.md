---
description: Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: Metodo ID3DXKeyframedAnimationSet::SetScaleKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5d33ab0c8e6bd01335d5843121917f89e3cf60bd81a5d54a85d298ec990e4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748210"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a>Metodo ID3DXKeyframedAnimationSet::SetScaleKey

Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
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

*pScaleKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntatore ai dati di scala. Vedere [**D3DXKEY \_ VECTOR3.**](d3dxkey-vector3.md)

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

 

 
