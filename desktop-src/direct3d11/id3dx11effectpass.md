---
title: Interfaccia ID3DX11EffectPass (D3dx11effect. h)
description: Un'interfaccia ID3DX11EffectPass incapsula le assegnazioni di stato all'interno di una tecnica. La durata di un oggetto ID3DX11EffectPass è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interfaccia ID3DX11EffectPass Direct3D 11
- Interfaccia ID3DX11EffectPass Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235152"
---
# <a name="id3dx11effectpass-interface"></a>Interfaccia ID3DX11EffectPass

Un'interfaccia **ID3DX11EffectPass** incapsula le assegnazioni di stato all'interno di una tecnica.

La durata di un oggetto **ID3DX11EffectPass** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectPass** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Applica**](id3dx11effectpass-apply.md)                                 | Impostare lo stato contenuto in un passaggio al dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Genera una maschera per consentire o impedire le modifiche di stato.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Ottenere un'annotazione in base all'indice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Ottenere un'annotazione in base al nome.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Ottenere una descrizione del compute shader.<br/>                      |
| [**Getdesc**](id3dx11effectpass-getdesc.md)                             | Ottenere una descrizione del passaggio.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Ottenere una descrizione dello shader di dominio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Ottenere una descrizione dello shader di geometria.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Ottenere la descrizione di Hull-shader.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Ottenere una descrizione del pixel shader.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Ottenere una descrizione del vertex shader.<br/>                       |
| [**isValid**](id3dx11effectpass-isvalid.md)                             | Testare un passaggio per verificare se contiene una sintassi valida.<br/>        |



 

## <a name="remarks"></a>Commenti

Un passaggio è un blocco di codice che imposta gli shader e gli oggetti dello stato di rendering. Una sessione viene dichiarata all'interno di una tecnica.

Per ottenere un'interfaccia Effect-Pass, chiamare un metodo come [**ID3DX11EffectTechnique:: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

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

 

 





