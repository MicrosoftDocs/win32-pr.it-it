---
description: Trasforma il vettore 3D normale dalla matrice specificata.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Funzione D3DXVec3TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235165"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a>Funzione D3DXVec3TransformNormal (D3dx9math. h)

Trasforma il vettore 3D normale dalla matrice specificata.

## <a name="syntax"></a>Sintassi


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.

</dd> <dt>

*PM* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore trasformato.

## <a name="remarks"></a>Commenti

Questa funzione trasforma il vettore (*PV*->x, *PV*->y, *PV*->z, 0) dalla matrice a cui punta il *PM*.

Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXVec3TransformNormal** può essere utilizzata come parametro per un'altra funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




