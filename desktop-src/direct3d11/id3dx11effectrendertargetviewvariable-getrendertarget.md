---
title: Metodo GetRenderTarget ID3DX11EffectRenderTargetViewVariable (D3dx11effect.h)
description: Ottenere una destinazione di rendering.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Metodo GetRenderTarget Direct3D 11
- Metodo GetRenderTarget Interfaccia Direct3D 11, ID3DX11EffectRenderTargetViewVariable
- ID3DX11EffectRenderTargetViewVariable interface Direct3D 11 , Metodo GetRenderTarget
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
ms.openlocfilehash: 035ea8f82ece3ca030099eb949f2fb08229c0a9c9b068f45237403b86cf92955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045869"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a>Metodo ID3DX11EffectRenderTargetViewVariable::GetRenderTarget

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

Indirizzo di un puntatore a un'interfaccia render-target-view. Vedere [**ID3D11RenderTargetView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





