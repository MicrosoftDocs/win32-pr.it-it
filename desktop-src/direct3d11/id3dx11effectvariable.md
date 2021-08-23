---
title: Interfaccia ID3DX11EffectVariable (D3dx11effect.h)
description: L'interfaccia ID3DX11EffectVariable è la classe di base per tutte le variabili di effetto. La durata di un oggetto ID3DX11EffectVariable è uguale alla durata dell'oggetto ID3DX11Effect padre.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- INTERFACCIA ID3DX11EffectVariable Direct3D 11
- ID3DX11EffectVariable interface Direct3D 11 , descritto
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3340ba231785edb9446c8578d886fca4a28ecbb09e69230d7f8661a5650afa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045809"
---
# <a name="id3dx11effectvariable-interface"></a>Interfaccia ID3DX11EffectVariable

**L'interfaccia ID3DX11EffectVariable** è la classe di base per tutte le variabili di effetto.

La durata di un **oggetto ID3DX11EffectVariable** è uguale alla durata dell'oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11EffectVariable** include questi metodi.



| Metodo                                                                           | Descrizione                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | Ottiene una variabile effect-blend.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Ottiene una variabile di istanza di classe.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Ottiene un buffer costante.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Ottiene una variabile depth-stencil.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Ottiene una variabile depth-stencil-view.<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | Ottenere una variabile di interfaccia.<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | Ottiene una variabile di matrice.<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Ottenere una variabile di rasterizzazione.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Ottiene una variabile render-target-view.<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | Ottenere una variabile del campionatore.<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | Ottenere una variabile scalare.<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | Ottenere una variabile shader.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Ottenere una variabile di risorsa shader.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Ottenere una variabile stringa.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Ottiene una variabile unordered-access-view.<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | Ottiene una variabile di vettore.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Ottiene un'annotazione in base all'indice.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Ottiene un'annotazione in base al nome.<br/>                  |
| [**GetDesc**](id3dx11effectvariable-getdesc.md)                                 | Ottenere una descrizione.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Ottiene un elemento della matrice.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Ottiene un membro della struttura in base all'indice.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Ottiene un membro della struttura in base al nome.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Ottenere un membro della struttura in base alla semantica.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Ottiene un buffer costante.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Recuperare i dati.<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Ottenere informazioni sul tipo.<br/>                       |
| [**isValid**](id3dx11effectvariable-isvalid.md)                                 | Confrontare il tipo di dati con i dati archiviati.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Impostare i dati.<br/>                                   |



 

## <a name="remarks"></a>Commenti

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

 

 





