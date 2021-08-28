---
description: Registrare i dati dei fotogrammi chiave di ridimensionamento, rotazione e traslazione (SRT) per un'animazione.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: Metodo ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys (D3dx9anim.h)
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
ms.openlocfilehash: 07ec4db0bb02eb0a177375fc37af67264f1368b2ab952c0b170580112e4dbf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987371"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>Metodo ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys

Registrare i dati dei fotogrammi chiave di ridimensionamento, rotazione e traslazione (SRT) per un'animazione.

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

*pName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome dell'animazione.

</dd> <dt>

*NumScaleKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di chiavi di scala.

</dd> <dt>

*NumRotationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di chiavi di rotazione.

</dd> <dt>

*NumTranslationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di chiavi di traduzione.

</dd> <dt>

*pScaleKeys* \[ Pollici\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo riempie con dati di scala.

</dd> <dt>

*pRotationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di [**quaternioni D3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) che il metodo riempie con dati di rotazione.

</dd> <dt>

*pTranslationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo riempie con i dati di traslazione.

</dd> <dt>

*pAnimationIndex* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Restituisce l'indice dell'animazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



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

 

 
