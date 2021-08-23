---
description: "Funzione D3DXQuaternionExp (D3DX10Math.h): calcola l'esponenziale."
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Funzione D3DXQuaternionExp (D3DX10Math.h)
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
ms.openlocfilehash: 61035976610cac4bb428687d9742b3a493e0ba458c8a050f4ad77891f01c26b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991131"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a>Funzione D3DXQuaternionExp (D3DX10Math.h)

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pQ* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore alla struttura D3DXQUATERNION di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a una struttura D3DXQUATERNION che rappresenta l'esponenziale.

## <a name="remarks"></a>Commenti

Questo metodo converte un quaternione puro in un quaternione unità. D3DXQuaternionExp prevede un quaternione puro, dove w viene ignorato nel calcolo (w == 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



dove v è la parte vettore di un quaternione.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la funzione D3DXQuaternionExp può essere usata come parametro per un'altra funzione.

Il [**metodo D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) può essere usato anche per configurare i punti di controllo di un quaternione.

Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
