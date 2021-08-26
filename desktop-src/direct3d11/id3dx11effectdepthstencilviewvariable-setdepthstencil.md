---
title: Metodo ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect.h)
description: Impostare una risorsa depth-stencil-view.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Metodo SetDepthStencil Direct3D 11
- Metodo SetDepthStencil Interfaccia Direct3D 11, ID3DX11EffectDepthStencilViewVariable
- ID3DX11EffectDepthStencilViewVariable interface Direct3D 11 , SetDepthStencil method
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae1e8b984bb15e083360ef99036549c534d8e047a2375ad0b0a6e5469b9191c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069681"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a>Metodo ID3DX11EffectDepthStencilViewVariable::SetDepthStencil

Impostare una risorsa depth-stencil-view.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pResource* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***

Puntatore a un'interfaccia depth-stencil-view. Vedere [**ID3D11DepthStencilView.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)

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

[ID3DX11EffectDepthStencilViewVariable](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





