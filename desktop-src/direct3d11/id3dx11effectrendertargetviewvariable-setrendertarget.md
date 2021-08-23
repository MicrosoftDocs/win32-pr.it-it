---
title: Metodo ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect.h)
description: Impostare una destinazione di rendering.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Metodo SetRenderTarget Direct3D 11
- Metodo SetRenderTarget Interfaccia Direct3D 11, ID3DX11EffectRenderTargetViewVariable
- ID3DX11EffectRenderTargetViewVariable interface Direct3D 11 , Metodo SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd36ddab704ab7ac78d78e7e7cf0c2262794df76730bc6f9019662c292abbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045849"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>Metodo ID3DX11EffectRenderTargetViewVariable::SetRenderTarget

Impostare una destinazione di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Puntatore a un'interfaccia render-target-view. Vedere [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





