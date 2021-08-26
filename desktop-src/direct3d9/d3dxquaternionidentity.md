---
description: Restituisce il quaternione di identità.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: Funzione D3DXQuaternionIdentity (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca40cf6e600d63d7f50403821b39d41ff88104c68587416370202d0bfc66ef5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986431"
---
# <a name="d3dxquaternionidentity-function"></a>Funzione D3DXQuaternionIdentity

Restituisce il quaternione di identità.

## <a name="syntax"></a>Sintassi


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che è il risultato dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il quaternione di identità.

## <a name="remarks"></a>Commenti

Dato un quaternione (x, y, z, w), la funzione **D3DXQuaternionIdentity** restituirà il quaternione (0, 0, 0, 1).

Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.* In questo modo, la **funzione D3DXQuaternionIdentity** può essere usata come parametro per un'altra funzione.

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

[**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




