---
description: Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'Metodo ID3DXPRTCompBuffer:: ExtractPCA (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322322"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>Metodo ID3DXPRTCompBuffer:: ExtractPCA

Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartPCA* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice iniziale per i coefficienti di proiezione PCA da estrarre dal buffer.

</dd> <dt>

*NumExtract* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di coefficienti di proiezione PCA da estrarre dal buffer.

</dd> <dt>

*pPCACoefficients* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntatore alla posizione in cui vengono scritti i coefficienti AP (Principal Component Analysis) del cluster. La dimensione dei dati scritti è (numero di campioni) \* (numero di coefficienti PCA).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
