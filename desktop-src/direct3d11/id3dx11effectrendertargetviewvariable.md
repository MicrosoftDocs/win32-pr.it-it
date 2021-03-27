---
title: Interfaccia ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Un'interfaccia di visualizzazione della destinazione di rendering accede a una destinazione di rendering.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interfaccia ID3DX11EffectRenderTargetViewVariable Direct3D 11, descritta
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
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982202"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>Interfaccia ID3DX11EffectRenderTargetViewVariable

Un'interfaccia di visualizzazione della destinazione di rendering accede a una destinazione di rendering.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectRenderTargetViewVariable** eredita da [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md). **ID3DX11EffectRenderTargetViewVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectRenderTargetViewVariable** dispone di questi metodi.



| Metodo                                                                                     | Descrizione                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**GetRenderTarget**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Ottenere una destinazione di rendering.<br/>            |
| [**GetRenderTargetArray**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Ottenere una matrice di destinazioni di rendering.<br/> |
| [**SetRenderTarget**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Impostare una destinazione di rendering.<br/>            |
| [**SetRenderTargetArray**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Impostare una matrice di destinazioni di rendering.<br/> |



 

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

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





