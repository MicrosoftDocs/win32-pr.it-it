---
description: Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'Metodo ID3DXKeyframedAnimationSet:: GetScaleKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323500"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>Metodo ID3DXKeyframedAnimationSet:: GetScaleKeys

Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice di animazione.

</dd> <dt>

*pScaleKeys* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo deve compilare con i dati della scala dell'animazione.

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

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
