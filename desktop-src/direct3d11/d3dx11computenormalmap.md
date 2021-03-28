---
title: Funzione D3DX11ComputeNormalMap (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, ComputeNormalMap.
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
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235134"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap (funzione)

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.

 

Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.

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

*pContext* \[ in\]
</dt> <dd>

Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a un'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*pSrcTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntatore a un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , che rappresenta la trama della mappa dell'altezza di origine.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Uno o più \_ flag normalmap D3DX che controllano la generazione di mappe normali.

</dd> <dt>

*Canale* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Un \_ flag del canale D3DX che specifica l'origine delle informazioni sull'altezza.

</dd> <dt>

*Ampiezza* \[ in\]
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale. I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.

</dd> <dt>

*pDestTexture* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Puntatore a un'interfaccia [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , che rappresenta la trama di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3. I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale. Il denominatore differenze centrale è hardcoded in 2,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

