---
description: Ottiene il buffer di dati che archivia i dati di animazione dei fotogrammi chiave compressi.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: Metodo ID3DXCompressedAnimationSet::GetCompressedData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3290dcc9e9baeaa688117d8a98918e7df814a34812cb66791b2c8021a50f788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987586"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>Metodo ID3DXCompressedAnimationSet::GetCompressedData

Ottiene il buffer di dati che archivia i dati di animazione dei fotogrammi chiave compressi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppCompressedData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore al buffer di [**dati ID3DXBuffer**](id3dxbuffer.md) che riceve i dati di animazione dei fotogrammi chiave compressi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




