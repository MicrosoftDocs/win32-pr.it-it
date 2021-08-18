---
description: 'Funzione D3DXQuaternionRotationMatrix (D3dx9math.h): compila un quaternione da una matrice di rotazione.'
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Funzione D3DXQuaternionRotationMatrix (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3ad57cc34a7b16b15c49195e39004094a33e2a168c7a3ff2f5f7eb77c267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988451"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a>Funzione D3DXQuaternionRotationMatrix (D3dx9math.h)

Compila un quaternione da una matrice di rotazione.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'operazione.

</dd> <dt>

*pM* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) creata da una matrice di rotazione.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXQuaternionRotationMatrix** può essere usata come parametro per un'altra funzione.

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




