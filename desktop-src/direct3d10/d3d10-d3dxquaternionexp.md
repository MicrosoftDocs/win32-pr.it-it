---
description: Calcola l'esponenziale.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Funzione D3DXQuaternionExp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762173"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a>Funzione D3DXQuaternionExp (D3DX10Math. h)

Calcola l'esponenziale.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*broncio* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*PQ* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore alla struttura D3DXQUATERNION di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a una struttura D3DXQUATERNION che rappresenta l'esponenziale.

## <a name="remarks"></a>Commenti

Questo metodo converte un quaternione puro in un quaternione di unità. D3DXQuaternionExp prevede un quaternione puro, in cui w viene ignorato nel calcolo (w = = 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



dove v è la parte di vettore di un quaternione.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio. In questo modo, la funzione D3DXQuaternionExp può essere utilizzata come parametro per un'altra funzione.

Il metodo [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) può essere usato anche per impostare i punti di controllo di un quaternione.

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

 

 
