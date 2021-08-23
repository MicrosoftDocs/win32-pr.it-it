---
title: Funzione D3DX11UnsetAllDeviceObjects (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota Invece di usare questa funzione, è consigliabile usare il metodo ClearState ID3D11DeviceContext.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Funzione D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e046bbb67cfaf5e13a22e5b704e202c21ebc8fa82dfde3a21fb83f09dfc3a345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535972"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>Funzione D3DX11UnsetAllDeviceObjects

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

> [!Note]  
> Anziché usare questa funzione, è consigliabile usare il [**metodo ID3D11DeviceContext::ClearState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate)

 

Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su **NULL.** Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurarsi che, quando si rilasciano tutte le risorse, nessuna di esse sia associata al dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntatore a [**un oggetto ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





