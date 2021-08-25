---
description: Restituisce il prodotto del punto di due quaternioni.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: Funzione D3DXQuaternionDot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f4e1c2759b5d8a80615fb02dc8636f848938bd480fe3feebc158abd4b70efc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986451"
---
# <a name="d3dxquaterniondot-function"></a>Funzione D3DXQuaternionDot

Restituisce il prodotto del punto di due quaternioni.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Prodotto del punto di due quaternioni.

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

 

 
