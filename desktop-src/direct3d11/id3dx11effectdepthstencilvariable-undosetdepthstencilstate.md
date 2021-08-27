---
title: Metodo ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState (D3dx11effect.h)
description: Ripristina uno stato impostato in depth stencil precedente.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Metodo UndoSetDepthStencilState Direct3D 11
- Metodo UndoSetDepthStencilState Interfaccia Direct3D 11, ID3DX11EffectDepthStencilVariable
- ID3DX11EffectDepthStencilVariable interface Direct3D 11 , UndoSetDepthStencilState method
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 626c430c268c7c8c63e006bdde9e62a49d139d2212e08d7a3e4cedeea3d31722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989817"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a>Metodo ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState

Ripristina uno stato impostato in depth stencil precedente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in una matrice di interfacce depth-stencil. Se è presente una sola interfaccia di stencil di profondità, usare 0.

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

