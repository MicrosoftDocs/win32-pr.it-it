---
description: Restituisce la lunghezza di un vettore 4D.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: Funzione D3DXVec4Length (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea16c6406c217f5e5d76af68a5da3a0c8bd17b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969526"
---
# <a name="d3dxvec4length-function"></a>D3DXVec4Length (funzione)

Restituisce la lunghezza di un vettore 4D.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PV* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Lunghezza del vettore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4LengthSq**](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
