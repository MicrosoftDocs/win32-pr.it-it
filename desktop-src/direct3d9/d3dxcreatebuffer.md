---
description: Crea un oggetto buffer.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: Funzione D3DXCreateBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ce0ab65eb3100d7be70741738767359265213ffc53a45490523bc8cf9c7a272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804605"
---
# <a name="d3dxcreatebuffer-function"></a>Funzione D3DXCreateBuffer

Crea un oggetto buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumBytes* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del buffer da creare, in byte.

</dd> <dt>

*ppBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer,**](id3dxbuffer.md) che rappresenta l'oggetto buffer creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
