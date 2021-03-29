---
title: Metodo ID3DX11EffectRenderTargetViewVariable GetRenderTarget (D3dx11effect. h)
description: Ottenere una destinazione di rendering.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Metodo GetRenderTarget Direct3D 11
- Metodo GetRenderTarget Direct3D 11, interfaccia ID3DX11EffectRenderTargetViewVariable
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, metodo GetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa86dd3a5c950e18ae97ba1987ee0f44b9f658c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996257"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a>Metodo ID3DX11EffectRenderTargetViewVariable:: GetRenderTarget

Ottenere una destinazione di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***

Indirizzo di un puntatore a un'interfaccia di visualizzazione della destinazione di rendering. Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





