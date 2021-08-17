---
description: Modifica il numero di campioni contenuti nel buffer.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: Metodo ID3DXPRTBuffer::Resize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c6da4c5de4b38f5fe86b36622b7032e10ffe1be794ee8990ba19362cfd77d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730074"
---
# <a name="id3dxprtbufferresize-method"></a>Metodo ID3DXPRTBuffer::Resize

Modifica il numero di campioni contenuti nel buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di campioni da contenuto nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, verrà restituito il valore E \_ OUTOFMEMORY seguente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
