---
description: Ricampiona un buffer ID3DXPRTBuffer di input e lo salva in un buffer di output. Questo metodo può essere usato per convertire un buffer dei vertici in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: Metodo ID3DXPRTEngine::ResampleBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa945be7b01c928a5dc8f5e44a6a31e8cb6d879be102145d25e03e7bef73f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729615"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Metodo ID3DXPRTEngine::ResampleBuffer

Ricampiona un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input e lo salva in un buffer di output. Questo metodo può essere usato per convertire un buffer dei vertici in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore al buffer [**ID3DXPRTBuffer di**](id3dxprtbuffer.md) input.

</dd> <dt>

*pBufferOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore al buffer [**ID3DXPRTBuffer di**](id3dxprtbuffer.md) output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




