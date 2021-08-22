---
description: Applica i dati di trama archiviati a un buffer di trama ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: Metodo ID3DXPRTBuffer::EvalGH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c01eee9659bc650c6e914f17932fd12dca703150d69908511c37b4d7e0a41cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493031"
---
# <a name="id3dxprtbufferevalgh-method"></a>Metodo ID3DXPRTBuffer::EvalGH

Applica i dati di grondaia trame archiviati a un buffer di trama [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, verrà restituito il valore seguente.

## <a name="remarks"></a>Commenti

Questo metodo esegue una chiamata interna a [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) per recuperare e applicare i dati di trame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




