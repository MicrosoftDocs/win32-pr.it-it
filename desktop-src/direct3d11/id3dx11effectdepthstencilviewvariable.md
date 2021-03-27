---
title: Interfaccia ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Un'interfaccia di profondità-stencil-visualizzazione-variabile accede a una visualizzazione stencil profondità.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interfaccia ID3DX11EffectDepthStencilViewVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235107"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a>Interfaccia ID3DX11EffectDepthStencilViewVariable

Un'interfaccia di profondità-stencil-visualizzazione-variabile accede a una visualizzazione stencil profondità.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectDepthStencilViewVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilViewVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectDepthStencilViewVariable** dispone di questi metodi.



| Metodo                                                                                     | Descrizione                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**GetDepthStencil**](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | Ottenere una risorsa di visualizzazione stencil profondità.<br/>            |
| [**GetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | Ottenere una matrice di risorse di visualizzazione degli stencil di profondità.<br/> |
| [**SetDepthStencil**](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | Impostare una risorsa di visualizzazione stencil profondità.<br/>            |
| [**SetDepthStencilArray**](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | Impostare una matrice di risorse di visualizzazione degli stencil di profondità.<br/> |



 

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

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





