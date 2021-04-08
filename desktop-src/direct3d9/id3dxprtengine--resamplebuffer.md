---
description: Ricampiona un buffer ID3DXPRTBuffer di input e lo salva in un buffer di output. Questo metodo può essere utilizzato per convertire un buffer di vertice in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Metodo ID3DXPRTEngine:: ResampleBuffer (D3DX9Mesh. h)'
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
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762292"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Metodo ID3DXPRTEngine:: ResampleBuffer

Ricampiona un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input e lo salva in un buffer di output. Questo metodo può essere utilizzato per convertire un buffer di vertice in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBufferIn* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore al buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input.

</dd> <dt>

*pBufferOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntatore al buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




