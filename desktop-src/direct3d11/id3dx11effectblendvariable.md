---
title: Interfaccia ID3DX11EffectBlendVariable (D3dx11effect. h)
description: L'interfaccia della variabile Blend accede allo stato di Blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11
- Interfaccia ID3DX11EffectBlendVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969513"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interfaccia ID3DX11EffectBlendVariable

L'interfaccia della variabile Blend accede allo stato di Blend.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectBlendVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectBlendVariable** dispone di questi metodi.



| Metodo                                                                    | Descrizione                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Ottenere un puntatore a una variabile di stato di Blend.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Ottenere un puntatore a un'interfaccia di stato di Blend.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Imposta lo stato di Blend di un effetto.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Ripristina uno stato di Blend impostato in precedenza.<br/>     |



 

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

 

 





