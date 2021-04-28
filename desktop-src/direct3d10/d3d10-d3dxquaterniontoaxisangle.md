---
description: "Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h): calcola l'asse e l'angolo di rotazione di un quaternione."
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108699"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>Funzione D3DXQuaternionToAxisAngle (D3DX10Math.h)

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

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Puntatore all'oggetto [**D3DXQUATERNION di origine.**](d3d10-d3dxquaternion.md)

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Questa funzione restituisce un puntatore a [**un oggetto D3DXVECTOR3**](d3d10-d3dxvector3.md) che identifica l'asse di rotazione del quaternione.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Questa funzione restituisce un puntatore a un valore FLOAT che identifica l'angolo di rotazione del quaternione in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

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

 

 
