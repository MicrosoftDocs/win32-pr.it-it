---
description: Riempie una matrice con dati chiave traslazionali usati per l'animazione con fotogrammi chiave.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: Metodo ID3DXKeyframedAnimationSet::GetTranslationKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39b2c086442b6a235730f9ec228b377f0a8b8f39a83d7c5043cfbca56dae2345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987361"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a>Metodo ID3DXKeyframedAnimationSet::GetTranslationKeys

Riempie una matrice con dati chiave traslazionali usati per l'animazione con fotogrammi chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice dell'animazione.

</dd> <dt>

*pTranslationKeys* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo deve riempire con i dati di traslazione dell'animazione.

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

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
