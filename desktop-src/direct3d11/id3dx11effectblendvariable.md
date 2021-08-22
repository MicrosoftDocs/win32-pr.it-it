---
title: Interfaccia ID3DX11EffectBlendVariable (D3dx11effect.h)
description: L'interfaccia blend-variable accede allo stato blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- INTERFACCIA ID3DX11EffectBlendVariable Direct3D 11
- ID3DX11EffectBlendVariable interface Direct3D 11 , descritto
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
ms.openlocfilehash: e84bd65c15c40c2e7ce44092baebdef66f17f2de8c1052589a984ff15c9f4b77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046459"
---
# <a name="id3dx11effectblendvariable-interface"></a>Interfaccia ID3DX11EffectBlendVariable

L'interfaccia blend-variable accede allo stato blend.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectBlendVariable** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectBlendVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectBlendVariable** include questi metodi.



| Metodo                                                                    | Descrizione                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetBackingStore**](id3dx11effectblendvariable-getbackingstore.md)     | Ottiene un puntatore a una variabile di stato di blend.<br/>  |
| [**GetBlendState**](id3dx11effectblendvariable-getblendstate.md)         | Ottenere un puntatore a un'interfaccia dello stato di blend.<br/> |
| [**SetBlendState**](id3dx11effectblendvariable-setblendstate.md)         | Imposta lo stato di fusione di un effetto.<br/>             |
| [**UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md) | Ripristina uno stato di blend impostato in precedenza.<br/>     |



 

## <a name="remarks"></a>Commenti

Quando un effetto viene letto in memoria, viene creata un'interfaccia [**ID3DX11EffectVariable.**](id3dx11effectvariable.md)

Le variabili di effetto vengono salvate in memoria nell'archivio di backup. Quando viene applicata una tecnica, i valori nell'archivio di backup vengono copiati nel dispositivo. È possibile usare uno di questi metodi per restituire lo stato.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Interfacce effetti 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





