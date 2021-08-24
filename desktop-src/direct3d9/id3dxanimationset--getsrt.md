---
description: Ottiene i valori di scala, rotazione e traslazione del set di animazioni.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: Metodo ID3DXAnimationSet::GetSRT (D3dx9anim.h)
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
ms.openlocfilehash: baa1b882972a91626b19194f83655ea1839877943f7463be8991167eb72d17fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791071"
---
# <a name="id3dxanimationsetgetsrt-method"></a>Metodo ID3DXAnimationSet::GetSRT

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

*PeriodicPosition* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Posizione del set di animazioni. La posizione può essere ottenuta chiamando [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).

</dd> <dt>

*Animazione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice dell'animazione.

</dd> <dt>

*pScale* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore al [**vettore D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni.

</dd> <dt>

*pRotation* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore al [**quaternione D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni.

</dd> <dt>

*pTranslation* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore al [**vettore D3DXVECTOR3**](d3dxvector3.md) che descrive la traslazione del set di animazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR.**](./d3dxerr.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
