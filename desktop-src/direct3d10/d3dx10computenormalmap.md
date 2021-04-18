---
description: Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Funzione D3DX10ComputeNormalMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d7318e6d00d921ba0d573eb6fb696eed6c6a58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322951"
---
# <a name="d3dx10computenormalmap-function"></a>D3DX10ComputeNormalMap (funzione)

Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrcTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Uno o più \_ flag normalmap D3DX che controllano la generazione di mappe normali.

</dd> <dt>

*Canale* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Un \_ flag del canale D3DX che specifica l'origine delle informazioni sull'altezza.

</dd> <dt>

*Ampiezza* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale. I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.

</dd> <dt>

*pDestTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3. I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale. Il denominatore differenze centrale è hardcoded in 2,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
