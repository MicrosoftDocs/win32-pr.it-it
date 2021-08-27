---
description: Moltiplica ogni valore nel buffer per un valore costante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: Metodo ID3DXPRTBuffer::ScaleBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5cba39f6816e301f2d36e21e6f81c7bb1f6bb4792fe4ea8017de5d452faf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801489"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>Metodo ID3DXPRTBuffer::ScaleBuffer

Moltiplica ogni valore nel buffer per un valore costante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Ridimensionamento* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valore costante utilizzato per ridimensionare il buffer. Ogni valore nel buffer viene sostituito dal prodotto di questo valore e dal valore del buffer originale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
