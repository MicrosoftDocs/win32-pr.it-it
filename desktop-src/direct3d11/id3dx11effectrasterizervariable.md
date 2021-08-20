---
title: Interfaccia ID3DX11EffectRasterizerVariable (D3dx11effect.h)
description: Un'interfaccia rasterizer-variable accede allo stato di rasterizzazione.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interfaccia Id3DX11EffectRasterizerVariable Direct3D 11
- INTERFACCIA ID3DX11EffectRasterizerVariable Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4653936edc3fd2181f875b3a848e401b8fa24d318a1e48df4fa06e462ae3cf19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534187"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>Interfaccia ID3DX11EffectRasterizerVariable

Un'interfaccia rasterizer-variable accede allo stato di rasterizzazione.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectRasterizerVariable** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectRasterizerVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectRasterizerVariable** include questi metodi.



| Metodo                                                                                   | Descrizione                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Ottenere un puntatore a una variabile che contiene lo stato rasteriser.<br/> |
| [**GetRasterizerState**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Ottenere un puntatore a un'interfaccia di rasterizzazione.<br/>                    |
| [**SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Imposta lo stato di rasterizzazione.<br/>                                  |
| [**UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Ripristina uno stato di rasterizzazione impostato in precedenza.<br/>                  |



 

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

 

 





