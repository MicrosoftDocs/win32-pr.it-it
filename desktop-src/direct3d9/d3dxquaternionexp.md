---
description: Calcola l'esponenziale.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Funzione D3DXQuaternionExp (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9cb5765e01c4fbbc6ab3785363425262ee491ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322496"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a>Funzione D3DXQuaternionExp (D3dx9math. h)

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*PQ* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a una struttura [**D3DXQUATERNION**](d3dxquaternion.md) che rappresenta l'esponenziale.

## <a name="remarks"></a>Commenti

Questo metodo converte un quaternione puro in un quaternione di unità. **D3DXQuaternionExp** prevede un quaternione puro, in cui w viene ignorato nel calcolo (w = = 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



dove v è la parte di vettore di un quaternione.

Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* . In questo modo, la funzione **D3DXQuaternionExp** può essere utilizzata come parametro per un'altra funzione.

Il metodo [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) può essere usato anche per impostare i punti di controllo di un quaternione.

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




