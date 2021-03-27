---
title: Metodo ID3DX11EffectDepthStencilVariable SetDepthStencilState (D3dx11effect. h)
description: Imposta lo stato del depth stencil.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Metodo SetDepthStencilState Direct3D 11
- Metodo SetDepthStencilState Direct3D 11, interfaccia ID3DX11EffectDepthStencilVariable
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, metodo SetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982454"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a>Metodo ID3DX11EffectDepthStencilVariable:: SetDepthStencilState

Imposta lo stato del depth stencil.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indicizzare in una matrice di interfacce di stencil di profondità. Se è presente una sola interfaccia di stencil Depth, usare 0.

</dd> <dt>

*pDepthStencilState* 
</dt> <dd>

Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***

Puntatore a un'interfaccia [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) contenente il nuovo stato depth stencil.

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

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

