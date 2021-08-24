---
description: 'Funzione D3DX10ComputeNormalMap: converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Funzione D3DX10ComputeNormalMap (D3DX10Tex.h)
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
ms.openlocfilehash: b719e1b40c3e8cd04ca0750e69c68bbd4a0a59394c3334818f091900606311af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634781"
---
# <a name="d3dx10computenormalmap-function"></a>Funzione D3DX10ComputeNormalMap

Converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.

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

*pSrcTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Uno o più flag D3DX \_ NORMALMAP che controllano la generazione di mappe normali.

</dd> <dt>

*Canale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Un flag CHANNEL D3DX \_ che specifica l'origine delle informazioni sull'altezza.

</dd> <dt>

*Ampiezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Moltiplicatore di valori costanti che aumenta o diminuisce i valori nella mappa normale. I valori più alti in genere rendono più visibili i rilievi, i valori più bassi in genere rendono i rilievi meno visibili.

</dd> <dt>

*pDestTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Puntatore a un'interfaccia ID3D10Texture2D, che rappresenta la trama di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo calcola la normale usando la differenza centrale con una dimensione del kernel di 3x3. I canali RGB nella destinazione contengono componenti distorti (x,y,z) della normale. Il denominatore differenze centrale è hardcoded a 2.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
