---
title: Interfaccia ID3DX11EffectTechnique (D3dx11effect. h)
description: Un'interfaccia ID3DX11EffectTechnique è una raccolta di passaggi. La durata di un oggetto ID3DX11EffectTechnique è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interfaccia ID3DX11EffectTechnique Direct3D 11
- Interfaccia ID3DX11EffectTechnique Direct3D 11, descritta
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
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982539"
---
# <a name="id3dx11effecttechnique-interface"></a>Interfaccia ID3DX11EffectTechnique

Un'interfaccia **ID3DX11EffectTechnique** è una raccolta di passaggi.

La durata di un oggetto **ID3DX11EffectTechnique** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectTechnique** dispone di questi metodi.



| Metodo                                                                        | Descrizione                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**ComputeStateBlockMask**](id3dx11effecttechnique-computestateblockmask.md) | Consente di calcolare una maschera a blocchi di stato per consentire o impedire modifiche di stato.<br/> |
| [**GetAnnotationByIndex**](id3dx11effecttechnique-getannotationbyindex.md)   | Ottenere un'annotazione in base all'indice.<br/>                                |
| [**GetAnnotationByName**](id3dx11effecttechnique-getannotationbyname.md)     | Ottenere un'annotazione in base al nome.<br/>                                 |
| [**Getdesc**](id3dx11effecttechnique-getdesc.md)                             | Ottenere una descrizione tecnica.<br/>                               |
| [**GetPassByIndex**](id3dx11effecttechnique-getpassbyindex.md)               | Ottenere un indice pass-by.<br/>                                       |
| [**GetPassByName**](id3dx11effecttechnique-getpassbyname.md)                 | Ottenere un passaggio per nome.<br/>                                        |
| [**isValid**](id3dx11effecttechnique-isvalid.md)                             | Testare una tecnica per verificare se contiene una sintassi valida.<br/>       |



 

## <a name="remarks"></a>Commenti

Un effetto contiene una o più tecniche. ogni tecnica contiene uno o più passaggi. ogni sessione contiene le assegnazioni di stato.

Per ottenere un'interfaccia effetto-tecnica, chiamare un metodo come [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





