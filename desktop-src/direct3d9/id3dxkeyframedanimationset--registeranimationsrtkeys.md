---
description: Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Metodo ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323492"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>Metodo ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys

Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'animazione.

</dd> <dt>

*NumScaleKeys* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di chiavi di scala.

</dd> <dt>

*NumRotationKeys* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di chiavi di rotazione.

</dd> <dt>

*NumTranslationKeys* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di chiavi di conversione.

</dd> <dt>

*pScaleKeys* \[ in\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo compila con i dati di ridimensionamento.

</dd> <dt>

*pRotationKeys* \[ in\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di quaternioni [**\_ Quaternion D3DXKEY**](d3dxkey-quaternion.md) che il metodo compila con i dati di rotazione.

</dd> <dt>

*pTranslationKeys* \[ in\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo compila con i dati di traduzione.

</dd> <dt>

*pAnimationIndex* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce l'indice di animazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
