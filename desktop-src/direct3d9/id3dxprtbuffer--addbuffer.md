---
description: Aggiunge un altro buffer a ID3DXPRTBuffer e archivia i risultati in ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: Metodo ID3DXPRTBuffer::AddBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffbaffbb47d91b18a6fad9bdee98012fa11fb923a7c7586acf7d7b0cd181bcc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294114"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>Metodo ID3DXPRTBuffer::AddBuffer

Aggiunge un altro buffer a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e archivia i risultati in **ID3DXPRTBuffer**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore a un buffer che contiene membri da aggiungere ai rispettivi membri del buffer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente.

## <a name="remarks"></a>Commenti

pBuffer e [**ID3DXPRTBuffer**](id3dxprtbuffer.md) devono avere lo stesso numero di campioni, coefficienti e canali di colore. In caso contrario, il metodo avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




