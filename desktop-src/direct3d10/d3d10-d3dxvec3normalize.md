---
description: 'Funzione D3DXVec3Normalize (D3DX10Math.h): restituisce la versione normalizzata di un vettore 3D.'
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Funzione D3DXVec3Normalize (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 88e6d129e123b043c5223a5a129ceb08ce7bb497bf5798cf48920dad8f86c9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989641"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a>Funzione D3DXVec3Normalize (D3DX10Math.h)

Restituisce la versione normalizzata di un vettore 3D.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore [**all'oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore alla struttura D3DXVECTOR3 di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a una struttura D3DXVECTOR3 che rappresenta la versione normalizzata del vettore specificato.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXVec3Normalize può essere usata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
