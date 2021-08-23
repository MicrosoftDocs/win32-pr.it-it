---
title: Interfaccia ID3DX11EffectRenderTargetViewVariable (D3dx11effect.h)
description: Un'interfaccia render-target-view accede a una destinazione di rendering.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interfaccia Direct3DX11EffectRenderTargetViewVariable Direct3D 11
- Id3DX11EffectRenderTargetViewVariable interface Direct3D 11 , descritto
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645f6253de34c3c4d2306a73f827dca59ae0ce7ce97e33df63edb592b3da651a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045839"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>Interfaccia ID3DX11EffectRenderTargetViewVariable

Un'interfaccia render-target-view accede a una destinazione di rendering.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectRenderTargetViewVariable** eredita da [**ID3DX11EffectRasterizerVariable.**](id3dx11effectvariable.md) **ID3DX11EffectRenderTargetViewVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectRenderTargetViewVariable** include questi metodi.



| Metodo                                                                                     | Descrizione                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Ottenere una destinazione di rendering.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Ottiene una matrice di destinazioni di rendering.<br/> |
| [**SetRenderTarget**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Impostare una destinazione di rendering.<br/>            |
| [**SetRenderTargetArray**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Impostare una matrice di destinazioni di rendering.<br/> |



 

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

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce effetti 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





