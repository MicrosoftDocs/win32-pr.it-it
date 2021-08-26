---
title: Interfaccia ID3DX11EffectSamplerVariable (D3dx11effect.h)
description: Un'interfaccia del campionatore accede allo stato del campionatore.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Id3DX11EffectSamplerVariable interface Direct3D 11
- ID3DX11EffectSamplerVariable interface Direct3D 11 , descritto
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
ms.openlocfilehash: d0865df924fb3a01e3c10ae015f13b4ec6e06e900dad32ff966d9bdbfed0c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952821"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interfaccia ID3DX11EffectSamplerVariable

Un'interfaccia del campionatore accede allo stato del campionatore.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11EffectSamplerVariable** eredita da [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectSamplerVariable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectSamplerVariable** include questi metodi.



| Metodo                                                                  | Descrizione                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Ottenere un puntatore a una variabile che contiene lo stato del campionatore.<br/> |
| [**GetSampler**](id3dx11effectsamplervariable-getsampler.md)           | Ottenere un puntatore a un'interfaccia del campionatore.<br/>                    |
| [**SetSampler**](id3dx11effectsamplervariable-setsampler.md)           | Impostare lo stato del campionatore.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Ripristinare uno stato del campionatore impostato in precedenza.<br/>                   |



 

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

 

 





