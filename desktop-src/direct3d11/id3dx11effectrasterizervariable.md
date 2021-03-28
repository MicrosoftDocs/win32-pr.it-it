---
title: Interfaccia ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Un'interfaccia di rasterizzatore-variabile accede allo stato di rasterizzazione.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11
- Interfaccia ID3DX11EffectRasterizerVariable Direct3D 11, descritta
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
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996260"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>Interfaccia ID3DX11EffectRasterizerVariable

Un'interfaccia di rasterizzatore-variabile accede allo stato di rasterizzazione.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectRasterizerVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectRasterizerVariable** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Ottiene un puntatore a una variabile che contiene lo stato rasteriser.<br/> |
| [**GetRasterizerState**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Ottenere un puntatore a un'interfaccia di rasterizzazione.<br/>                    |
| [**SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Imposta lo stato del rasterizzatore.<br/>                                  |
| [**UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Ripristina uno stato di rasterizzazione impostato in precedenza.<br/>                  |



 

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

 

 





