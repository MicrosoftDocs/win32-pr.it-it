---
description: Compila un quaternione da una matrice di rotazione.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Funzione D3DXQuaternionRotationMatrix (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235156"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a>Funzione D3DXQuaternionRotationMatrix (D3DX10Math. h)

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

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore alla struttura D3DXQUATERNION compilata da una matrice di rotazione.

## <a name="remarks"></a>Commenti

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXQuaternionRotationMatrix può essere utilizzata come parametro per un'altra funzione.

Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
