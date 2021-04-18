---
description: Restituisce il quadrato della lunghezza di un quaternione.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Funzione D3DXQuaternionLengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323307"
---
# <a name="d3dxquaternionlengthsq-function"></a>D3DXQuaternionLengthSq (funzione)

Restituisce il quadrato della lunghezza di un quaternione.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PQ* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Lunghezza quadrata del quaternione.

## <a name="remarks"></a>Commenti

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

[**D3DXQuaternionLength**](d3dxquaternionlength.md)
</dt> </dl>

 

 
