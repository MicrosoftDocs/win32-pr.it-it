---
title: Interfaccia ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Un'interfaccia della variabile di stencil Depth accede allo stato di stencil Depth.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11
- Interfaccia ID3DX11EffectDepthStencilVariable Direct3D 11, descritta
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
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969469"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Interfaccia ID3DX11EffectDepthStencilVariable

Un'interfaccia della variabile di stencil Depth accede allo stato di stencil Depth.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectDepthStencilVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectDepthStencilVariable** dispone di questi metodi.



| Metodo                                                                                         | Descrizione                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Ottenere un puntatore a una variabile che contiene lo stato di stencil Depth.<br/> |
| [**GetDepthStencilState**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Ottenere un puntatore a un'interfaccia di stencil profondità.<br/>                    |
| [**SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Imposta lo stato del depth stencil.<br/>                                  |
| [**UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Ripristina uno stato di depth stencil impostato in precedenza.<br/>                  |



 

## <a name="remarks"></a>Commenti

Un'interfaccia [**ID3DX11EffectVariable**](id3dx11effectvariable.md) viene creata quando un effetto viene letto in memoria.

Le variabili di effetto vengono salvate in memoria nell'archivio di backup; Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. È possibile usare uno di questi metodi per restituire lo stato.

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

 

 





