---
description: 'Funzione D3DXQuaternionMultiply (D3DX10Math.h): moltiplica due quaternioni.'
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Funzione D3DXQuaternionMultiply (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 87d1b386409047eefc3e70ce5007082dda2158122ccfe4e2d3b2bea683a25a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991091"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a>Funzione D3DXQuaternionMultiply (D3DX10Math.h)

Moltiplica due quaternioni.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***

Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pQ1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Puntatore a una [**struttura D3DXQUATERNION di**](d3d10-d3dxquaternion.md) origine.

</dd> <dt>

*pQ2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***

Puntatore a una [**struttura D3DXQUATERNION di**](d3d10-d3dxquaternion.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Puntatore a [**una struttura D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il prodotto di due quaternioni.

## <a name="remarks"></a>Commenti

Il risultato rappresenta la rotazione Q1 seguita dalla rotazione Q2 (Out = Q2 \* Q1). Questa operazione viene eseguita in modo che **D3DXQuaternionMultiply** mantenga la stessa semantica di [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) perché i quaternioni di unità possono essere considerati come un altro modo per rappresentare le matrici di rotazione.

Le trasformazioni vengono concatenate nello stesso ordine per entrambe le funzioni **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply.**](d3d10-d3dxmatrixmultiply.md) Ad esempio, supponendo che mX e mY rappresentino le stesse rotazioni di qX e qY, sia m che q rappresenteranno le stesse rotazioni.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



La moltiplicazione dei quaternioni non è commutativa.

Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut. In questo modo, la **funzione D3DXQuaternionMultiply** può essere usata come parametro per un'altra funzione.

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

 

 
