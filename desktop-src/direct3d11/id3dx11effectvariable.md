---
title: Interfaccia ID3DX11EffectVariable (D3dx11effect. h)
description: L'interfaccia ID3DX11EffectVariable è la classe di base per tutte le variabili di effetto. La durata di un oggetto ID3DX11EffectVariable è uguale alla durata del relativo oggetto ID3DX11Effect padre.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interfaccia ID3DX11EffectVariable Direct3D 11
- Interfaccia ID3DX11EffectVariable Direct3D 11, descritta
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
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762197"
---
# <a name="id3dx11effectvariable-interface"></a>Interfaccia ID3DX11EffectVariable

L'interfaccia **ID3DX11EffectVariable** è la classe di base per tutte le variabili di effetto.

La durata di un oggetto **ID3DX11EffectVariable** è uguale alla durata del relativo oggetto [**ID3DX11Effect**](id3dx11effect.md) padre.

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11EffectVariable** dispone di questi metodi.



| Metodo                                                                           | Descrizione                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**AsBlend**](id3dx11effectvariable-asblend.md)                                 | Ottenere una variabile Effect-Blend.<br/>                |
| [**AsClassInstance**](id3dx11effectvariable-asclassinstance.md)                 | Ottenere una variabile di istanza di classe.<br/>              |
| [**AsConstantBuffer**](id3dx11effectvariable-asconstantbuffer.md)               | Ottenere un buffer costante.<br/>                      |
| [**AsDepthStencil**](id3dx11effectvariable-asdepthstencil.md)                   | Ottenere una variabile di stencil Depth.<br/>               |
| [**AsDepthStencilView**](id3dx11effectvariable-asdepthstencilview.md)           | Ottenere una variabile depth-stencil-View.<br/>          |
| [**AsInterface**](id3dx11effectvariable-asinterface.md)                         | Ottiene una variabile di interfaccia.<br/>                  |
| [**AsMatrix**](id3dx11effectvariable-asmatrix.md)                               | Ottenere una variabile di matrice.<br/>                      |
| [**AsRasterizer**](id3dx11effectvariable-asrasterizer.md)                       | Ottiene una variabile di rasterizzazione.<br/>                  |
| [**AsRenderTargetView**](id3dx11effectvariable-asrendertargetview.md)           | Ottenere una variabile di visualizzazione della destinazione di rendering.<br/>          |
| [**AsSampler**](id3dx11effectvariable-assampler.md)                             | Ottiene una variabile del campionatore.<br/>                     |
| [**AsScalar**](id3dx11effectvariable-asscalar.md)                               | Ottenere una variabile scalare.<br/>                      |
| [**AsShader**](id3dx11effectvariable-asshader.md)                               | Ottiene una variabile shader.<br/>                      |
| [**AsShaderResource**](id3dx11effectvariable-asshaderresource.md)               | Ottenere una variabile di risorsa shader.<br/>             |
| [**AsString**](id3dx11effectvariable-asstring.md)                               | Ottiene una variabile di stringa.<br/>                      |
| [**AsUnorderedAccessView**](id3dx11effectvariable-asunorderedaccessview.md)     | Ottenere una variabile di visualizzazione non ordinata.<br/>      |
| [**AsVector**](id3dx11effectvariable-asvector.md)                               | Ottenere una variabile vettoriale.<br/>                      |
| [**GetAnnotationByIndex**](id3dx11effectvariable-getannotationbyindex.md)       | Ottenere un'annotazione in base all'indice.<br/>                 |
| [**GetAnnotationByName**](id3dx11effectvariable-getannotationbyname.md)         | Ottenere un'annotazione in base al nome.<br/>                  |
| [**Getdesc**](id3dx11effectvariable-getdesc.md)                                 | Ottenere una descrizione.<br/>                          |
| [**GetElement**](id3dx11effectvariable-getelement.md)                           | Ottiene un elemento di matrice.<br/>                       |
| [**GetMemberByIndex**](id3dx11effectvariable-getmemberbyindex.md)               | Ottiene un membro della struttura in base all'indice.<br/>            |
| [**GetMemberByName**](id3dx11effectvariable-getmemberbyname.md)                 | Ottenere un membro della struttura in base al nome.<br/>             |
| [**GetMemberBySemantic**](id3dx11effectvariable-getmemberbysemantic.md)         | Ottenere un membro della struttura in base alla semantica.<br/>         |
| [**GetParentConstantBuffer**](id3dx11effectvariable-getparentconstantbuffer.md) | Ottenere un buffer costante.<br/>                      |
| [**GetRawValue**](id3dx11effectvariable-getrawvalue.md)                         | Recuperare i dati.<br/>                                   |
| [**GetType**](id3dx11effectvariable-gettype.md)                                 | Ottenere informazioni sul tipo.<br/>                       |
| [**isValid**](id3dx11effectvariable-isvalid.md)                                 | Confrontare il tipo di dati con i dati archiviati.<br/> |
| [**SetRawValue**](id3dx11effectvariable-setrawvalue.md)                         | Impostare i dati.<br/>                                   |



 

## <a name="remarks"></a>Commenti

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

 

 





