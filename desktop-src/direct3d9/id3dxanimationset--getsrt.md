---
description: Ottiene i valori di scala, rotazione e traslazione del set di animazioni.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'Metodo ID3DXAnimationSet:: GetSRT (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323616"
---
# <a name="id3dxanimationsetgetsrt-method"></a>Metodo ID3DXAnimationSet:: GetSRT

Ottiene i valori di scala, rotazione e traslazione del set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PeriodicPosition* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posizione del set di animazioni. La posizione può essere ottenuta chiamando [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).

</dd> <dt>

*Animazione* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice di animazione.

</dd> <dt>

*pScale* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore al vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni.

</dd> <dt>

*protazione* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore al quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni.

</dd> <dt>

*pTranslation* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore al vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la traduzione del set di animazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
