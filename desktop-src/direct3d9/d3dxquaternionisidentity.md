---
description: Determina se un quaternione è un quaternione di identità.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Funzione D3DXQuaternionIsIdentity (D3dx9math.h)
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
ms.openlocfilehash: b34debbe70ec6edcd3f08a1ec83383335a0d4f97801d122bc1bd73a82a81ff36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731593"
---
# <a name="d3dxquaternionisidentity-function"></a>Funzione D3DXQuaternionIsIdentity

Determina se un quaternione è un quaternione di identità.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pQ* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che verrà testata per l'identità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se il quaternione è un quaternione di identità, questa funzione restituisce **TRUE.** In caso contrario, questa funzione restituisce **FALSE.**

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
</dt> <dt>

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
