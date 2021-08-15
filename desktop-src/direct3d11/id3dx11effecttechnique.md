---
title: Interfaccia ID3DX11EffectTechnique (D3dx11effect.h)
description: Un'interfaccia ID3DX11EffectTechnique è una raccolta di passaggi. La durata di un oggetto ID3DX11EffectTechnique è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique interface Direct3D 11
- ID3DX11EffectTechnique interface Direct3D 11 , descritto
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d8970ad1e75f37e8270a013d3830216ae128e41c03d4ad5245ac6ffc7615691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532353"
---
# <a name="id3dx11effecttechnique-interface"></a>Interfaccia ID3DX11EffectTechnique

**Un'interfaccia ID3DX11EffectTechnique** è una raccolta di passaggi.

La durata di un **oggetto ID3DX11EffectTechnique** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectTechnique** include questi metodi.



| Metodo                                                                        | Descrizione                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Calcolare una maschera di blocco di stato per consentire o impedire modifiche dello stato.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Ottiene un'annotazione in base all'indice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Ottiene un'annotazione in base al nome.<br/>                                 |
| [**GetDesc**](id3dx11effecttechnique-getdesc.md)                             | Ottenere una descrizione della tecnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Ottenere un passaggio per indice.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Ottenere un pass by name.<br/>                                        |
| [**isValid**](id3dx11effecttechnique-isvalid.md)                             | Testare una tecnica per verificare se contiene una sintassi valida.<br/>       |



 

## <a name="remarks"></a>Commenti

Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi. ogni passaggio contiene assegnazioni di stato.

Per ottenere un'interfaccia di tecnica dell'effetto, chiamare un metodo come [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce effetti 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





