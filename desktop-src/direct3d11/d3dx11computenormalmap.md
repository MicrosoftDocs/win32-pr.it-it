---
title: Funzione D3DX11ComputeNormalMap (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare la libreria DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Funzione D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124916"
---
# <a name="d3dx11computenormalmap-function"></a>Funzione D3DX11ComputeNormalMap

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Invece di usare questa funzione, è consigliabile usare la [libreria DirectXTex,](https://github.com/Microsoft/DirectXTex) **ComputeNormalMap.**

 

Converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a [**un'interfaccia ID3D11DeviceContext,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*pSrcTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntatore a [**un'interfaccia ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Uno o più flag D3DX \_ NORMALMAP che controllano la generazione di mappe normali.

</dd> <dt>

*Canale* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Un flag CHANNEL D3DX \_ che specifica l'origine delle informazioni sull'altezza.

</dd> <dt>

*Ampiezza* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

Moltiplicatore di valori costante che aumenta (o diminuisce) i valori nella mappa normale. I valori più elevati in genere rendono le dossi più visibili, i valori più bassi in genere rendono le dossi meno visibili.

</dd> <dt>

*pDestTexture* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntatore a [**un'interfaccia ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) che rappresenta la trama di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo calcola la normale usando la differenza centrale con una dimensione del kernel di 3x3. I canali RGB nella destinazione contengono componenti parziali (x,y,z) della normale. Il denominatore differenze centrale è hardcoded a 2.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

