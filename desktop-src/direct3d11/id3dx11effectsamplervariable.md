---
title: Interfaccia ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Un'interfaccia del campionatore accede allo stato del campionatore.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11
- Interfaccia ID3DX11EffectSamplerVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132410"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interfaccia ID3DX11EffectSamplerVariable

Un'interfaccia del campionatore accede allo stato del campionatore.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11EffectSamplerVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectSamplerVariable** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Ottiene un puntatore a una variabile che contiene lo stato del campionatore.<br/> |
| [**Getsampler**](id3dx11effectsamplervariable-getsampler.md)           | Ottenere un puntatore a un'interfaccia del campionatore.<br/>                    |
| [**Sesampler**](id3dx11effectsamplervariable-setsampler.md)           | Impostare lo stato del campionatore.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Ripristinare uno stato del campionatore impostato in precedenza.<br/>                   |



 

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

 

 





