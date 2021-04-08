---
description: Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Metodo ID3DXKeyframedAnimationSet:: GetRotationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762310"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a>Metodo ID3DXKeyframedAnimationSet:: GetRotationKeys

Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice di animazione.

</dd> <dt>

*pRotationKeys* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**

Puntatore a una matrice allocata dall'utente di quaternioni [**\_ Quaternion D3DXKEY**](d3dxkey-quaternion.md) che il metodo deve compilare con i dati di rotazione dell'animazione.

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

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
