---
description: Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'Metodo ID3DXKeyframedAnimationSet:: UnregisterScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969494"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a>Metodo ID3DXKeyframedAnimationSet:: UnregisterScaleKey

Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Animazione* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificatore dell'animazione.

</dd> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Fotogramma chiave.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo è lento e non deve essere usato dopo che è iniziata la riproduzione di un'animazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
