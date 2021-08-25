---
title: Interfaccia ID3DX11Effect (D3dx11effect.h)
description: Un'interfaccia ID3DX11Effect gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- INTERFACCIA ID3DX11Effect Direct3D 11
- INTERFACCIA ID3DX11Effect Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479147"
---
# <a name="id3dx11effect-interface"></a>Interfaccia ID3DX11Effect

**Un'interfaccia ID3DX11Effect** gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11Effect** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11Effect** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11Effect** include questi metodi.



| Metodo                                                                     | Descrizione                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Crea una copia di un'interfaccia effetto.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Ottiene un'interfaccia di collegamento della classe.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Ottiene un buffer costante in base all'indice.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Ottenere un buffer costante in base al nome.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Ottenere una descrizione dell'effetto.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Ottenere il dispositivo che ha creato l'effetto.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Ottiene un gruppo di effetti in base all'indice.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Ottiene un gruppo di effetti in base al nome.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Ottenere una tecnica in base all'indice.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Ottenere una tecnica in base al nome.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Ottenere una variabile in base all'indice.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Ottenere una variabile in base al nome.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Ottenere una variabile in base alla semantica.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Testare un effetto per verificare se i metadati di reflection sono stati rimossi dalla memoria.<br/> |
| [**isValid**](id3dx11effect-isvalid.md)                                   | Testare un effetto per verificare se contiene una sintassi valida.<br/>                             |
| [**Ottimizzazione**](id3dx11effect-optimize.md)                                 | Ridurre al minimo la quantità di memoria necessaria per un effetto.<br/>                          |



 

## <a name="remarks"></a>Commenti

Un effetto viene creato chiamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

Il sistema di effetti raggruppa le informazioni necessarie per il rendering in un effetto che contiene: oggetti di stato per l'assegnazione di modifiche dello stato nei gruppi, risorse per fornire dati di input e archiviare dati di output e programmi che controllano come viene eseguito il rendering chiamati shader.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

> [!Note]
>
> Se si chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su **un oggetto ID3DX11Effect** per recuperare l'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **QueryInterface** restituisce E \_ NOINTERFACE. Per risolvere questo problema, usare il codice seguente:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>Requisiti

| Requisito | valore |
|-------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Interfacce di Effects 11](d3d11-graphics-reference-effects11-interfaces.md)

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
