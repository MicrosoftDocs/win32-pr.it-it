---
description: 'Funzione D3DXQuaternionMultiply (D3dx9math.h): moltiplica due quaternioni.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Funzione D3DXQuaternionMultiply (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4fe5c7f6d95bef19ce77e7ea7815e6808eae63e7643bbfc40e6b0fa1bb45767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750071"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a>Funzione D3DXQuaternionMultiply (D3dx9math.h)

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.

</dd> <dt>

*pQ1* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.

</dd> <dt>

*pQ2* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il prodotto di due quaternioni.

## <a name="remarks"></a>Commenti

Il risultato rappresenta la rotazione Q1 seguita dalla rotazione Q2 (Out = Q2 \* Q1). Questa operazione viene eseguita in modo che **D3DXQuaternionMultiply** mantenga la stessa semantica di [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) perché i quaternioni di unità possono essere considerati come un altro modo per rappresentare le matrici di rotazione.

Le trasformazioni vengono concatenate nello stesso ordine per entrambe le funzioni **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply.**](d3dxmatrixmultiply.md) Ad esempio, supponendo che mX e mY rappresentino le stesse rotazioni di qX e qY, sia m che q rappresenteranno le stesse rotazioni.


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



La moltiplicazione dei quaternioni non è commutativa.

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXQuaternionMultiply** può essere usata come parametro per un'altra funzione.

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

[**D3DXMatrixMultiply**](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




