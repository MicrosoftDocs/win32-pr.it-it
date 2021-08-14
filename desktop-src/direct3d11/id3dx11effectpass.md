---
title: Interfaccia ID3DX11EffectPass (D3dx11effect.h)
description: Un'interfaccia ID3DX11EffectPass incapsula le assegnazioni di stato all'interno di una tecnica. La durata di un oggetto ID3DX11EffectPass è uguale alla durata dell'oggetto ID3DX11Effect padre.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- INTERFACCIA ID3DX11EffectPass Direct3D 11
- INTERFACCIA ID3DX11EffectPass Direct3D 11 , descritta
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
ms.openlocfilehash: 33b24fe0154e447cd993e8e7e939a9a023ed37183a56980dab8f5d803a0ea41e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045976"
---
# <a name="id3dx11effectpass-interface"></a>Interfaccia ID3DX11EffectPass

**Un'interfaccia ID3DX11EffectPass** incapsula le assegnazioni di stato all'interno di una tecnica.

La durata di un **oggetto ID3DX11EffectPass** è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectPass** include questi metodi.



| Metodo                                                                   | Descrizione                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Applica**](id3dx11effectpass-apply.md)                                 | Impostare lo stato contenuto in un passaggio al dispositivo.<br/>       |
| [**ComputeStateBlockMask**](id3dx11effectpass-computestateblockmask.md) | Generare una maschera per consentire o impedire modifiche dello stato.<br/> |
| [**GetAnnotationByIndex**](id3dx11effectpass-getannotationbyindex.md)   | Ottiene un'annotazione in base all'indice.<br/>                            |
| [**GetAnnotationByName**](id3dx11effectpass-getannotationbyname.md)     | Ottenere un'annotazione in base al nome.<br/>                             |
| [**GetComputeShaderDesc**](id3dx11effectpass-getcomputeshaderdesc.md)   | Ottenere una descrizione dello shader di calcolo.<br/>                      |
| [**GetDesc**](id3dx11effectpass-getdesc.md)                             | Ottenere una descrizione del passaggio.<br/>                                |
| [**GetDomainShaderDesc**](id3dx11effectpass-getdomainshaderdesc.md)     | Ottenere una descrizione dello shader di dominio.<br/>                       |
| [**GetGeometryShaderDesc**](id3dx11effectpass-getgeometryshaderdesc.md) | Ottenere una descrizione geometry-shader.<br/>                     |
| [**GetHullShaderDesc**](id3dx11effectpass-gethullshaderdesc.md)         | Ottenere la descrizione dello hull shader.<br/>                           |
| [**GetPixelShaderDesc**](id3dx11effectpass-getpixelshaderdesc.md)       | Ottenere una descrizione di pixel shader.<br/>                        |
| [**GetVertexShaderDesc**](id3dx11effectpass-getvertexshaderdesc.md)     | Ottenere una descrizione di vertex shader.<br/>                       |
| [**isValid**](id3dx11effectpass-isvalid.md)                             | Testare un passaggio per verificare se contiene una sintassi valida.<br/>        |



 

## <a name="remarks"></a>Commenti

Un passaggio è un blocco di codice che imposta gli oggetti e gli shader dello stato di rendering. Un passaggio viene dichiarato all'interno di una tecnica.

Per ottenere un'interfaccia effect-pass, chiamare un metodo come [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Effects 11](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





