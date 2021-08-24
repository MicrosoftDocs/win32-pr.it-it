---
description: Blocca un intervallo di dati di esempio vertice o texel e ottiene un puntatore alla posizione nella memoria buffer.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: Metodo ID3DXPRTBuffer::LockBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d8e3b6310951a5784af99b913298c20d5556baa10b012926f3b68e44d402dbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606891"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>Metodo ID3DXPRTBuffer::LockBuffer

Blocca un intervallo di dati di esempio vertice o texel e ottiene un puntatore alla posizione nella memoria buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Avvio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice del campione di dati vertice o texel.

</dd> <dt>

*NumSamples* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici (o texel) campionati.

</dd> <dt>

*ppData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\*\***

Puntatore alla posizione in memoria in cui inizia l'esempio Start. Il layout della memoria dei dati del buffer è:


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente:

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumChannels**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumSamples**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
