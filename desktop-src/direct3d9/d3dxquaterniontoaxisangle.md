---
description: "Funzione D3DXQuaternionToAxisAngle (D3dx9math.h): calcola l'asse e l'angolo di rotazione di un quaternione."
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Funzione D3DXQuaternionToAxisAngle (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b22b0a4c094a47e412172807c42cf25dc3c89342cf8e7e4ece9e731d9014bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731289"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>Funzione D3DXQuaternionToAxisAngle (D3dx9math.h)

Calcola l'asse e l'angolo di rotazione di un quaternione.

## <a name="syntax"></a>Sintassi


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pQ* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore alla struttura [**D3DXQUATERNION di**](d3dxquaternion.md) origine.

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Questa funzione restituisce un puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che identifica l'asse di rotazione del quaternione.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Questa funzione restituisce un puntatore a un valore FLOAT che identifica l'angolo di rotazione del quaternione in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
