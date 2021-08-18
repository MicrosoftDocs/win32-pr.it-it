---
title: Interfaccia ID3DX11EffectDepthStencilVariable (D3dx11effect.h)
description: Un'interfaccia depth-stencil-variable accede allo stato depth-stencil.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- INTERFACCIA ID3DX11EffectDepthStencilVariable Direct3D 11
- ID3DX11EffectDepthStencilVariable interface Direct3D 11 , descritto
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d743bfebfa9722261d220800a633bdc8b268a520b883c9fea11f9f7948f7bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989771"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interfaccia ID3DX11EffectDepthStencilVariable

Un'interfaccia depth-stencil-variable accede allo stato depth-stencil.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectDepthStencilVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ID3DX11EffectDepthStencilVariable.**



| Metodo                                                                                         | Descrizione                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Ottiene un puntatore a una variabile che contiene lo stato depth-stencil.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Ottenere un puntatore a un'interfaccia depth-stencil.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Imposta lo depth stencil stato.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Ripristina uno stato di depth stencil impostato in precedenza.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando un effetto viene letto in memoria, viene creata un'interfaccia [**ID3DX11EffectVariable.**](id3dx11effectvariable.md)

Le variabili di effetto vengono salvate in memoria nell'archivio di backup. Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. È possibile usare uno di questi metodi per restituire lo stato.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce di Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





