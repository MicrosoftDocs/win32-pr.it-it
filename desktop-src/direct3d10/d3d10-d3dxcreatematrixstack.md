---
description: Creare uno stack di matrici.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: Funzione D3DXCreateMatrixStack (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b5799632f171d1b80f95f0f684bb22d24f741f6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402001"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a>Funzione D3DXCreateMatrixStack (D3DX10Math. h)

Creare uno stack di matrici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Non implementato. Specificare zero.

</dd> <dt>

*ppStack* \[ out\]
</dt> <dd>

Tipo: **LPD3DXMATRIXSTACK \***

Indirizzo di un puntatore a uno stack di matrici (vedere [**interfaccia ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
