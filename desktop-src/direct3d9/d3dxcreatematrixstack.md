---
description: Crea un'istanza dell'interfaccia ID3DXMATRIXStack.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: Funzione D3DXCreateMatrixStack (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323252"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a>Funzione D3DXCreateMatrixStack (D3dx9math. h)

Crea un'istanza dell'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Non implementato. Specificare zero.

</dd> <dt>

*ppStack* \[ out\]
</dt> <dd>

Tipo: **LPD3DXMATRIXSTACK \***

Indirizzo di un puntatore riempito con un puntatore a interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) se la funzione ha esito positivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
