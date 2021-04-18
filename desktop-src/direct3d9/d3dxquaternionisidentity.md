---
description: Determina se un quaternione è un quaternione di identità.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Funzione D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323308"
---
# <a name="d3dxquaternionisidentity-function"></a>D3DXQuaternionIsIdentity (funzione)

Determina se un quaternione è un quaternione di identità.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PQ* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che verrà testata per l'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se il quaternione è un quaternione Identity, questa funzione restituisce **true**. In caso contrario, la funzione restituisce **false**.

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

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
