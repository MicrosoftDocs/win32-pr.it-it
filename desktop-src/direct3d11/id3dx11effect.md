---
title: Interfaccia ID3DX11Effect (D3dx11effect. h)
description: Un'interfaccia ID3DX11Effect gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interfaccia ID3DX11Effect Direct3D 11
- Interfaccia ID3DX11Effect Direct3D 11, descritta
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
ms.openlocfilehash: 51c9b945f09ad0424ecd6b546aefe68bea276ffc
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314454"
---
# <a name="id3dx11effect-interface"></a>Interfaccia ID3DX11Effect

Un'interfaccia **ID3DX11Effect** gestisce un set di oggetti di stato, risorse e shader per l'implementazione di un effetto di rendering.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11Effect** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11Effect** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11Effect** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Crea una copia di un'interfaccia effetto.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Ottiene un'interfaccia di collegamento di classe.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Ottenere un buffer costante in base all'indice.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Ottenere un buffer costante in base al nome.<br/>                                                 |
| [**Getdesc**](id3dx11effect-getdesc.md)                                   | Ottenere una descrizione dell'effetto.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Ottenere il dispositivo che ha creato l'effetto.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Ottiene un effetto Group by index.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Ottiene un gruppo di effetti per nome.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Ottenere una tecnica in base all'indice.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Ottenere una tecnica in base al nome.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Ottiene una variabile in base all'indice.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Ottenere una variabile in base al nome.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Ottenere una variabile in base alla semantica.<br/>                                                    |
| [**Ottimizzato**](id3dx11effect-isoptimized.md)                           | Testare un effetto per verificare se i metadati della reflection sono stati rimossi dalla memoria.<br/> |
| [**isValid**](id3dx11effect-isvalid.md)                                   | Testare un effetto per verificare se contiene una sintassi valida.<br/>                             |
| [**Ottimizzare**](id3dx11effect-optimize.md)                                 | Ridurre al minimo la quantità di memoria necessaria per un effetto.<br/>                          |



 

## <a name="remarks"></a>Commenti

Un effetto viene creato chiamando [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

Il sistema di effetti raggruppa le informazioni necessarie per il rendering in un effetto che contiene gli oggetti di stato per l'assegnazione delle modifiche di stato nei gruppi, le risorse per fornire i dati di input e l'archiviazione dei dati di output e i programmi che controllano il modo in cui viene eseguito il rendering denominato shader.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

> [!Note]
>
> Se si chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un oggetto **ID3DX11Effect** per recuperare l'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** restituisce E \_ nointerface. Per risolvere questo problema, usare il codice seguente:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>>
>  

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------|-------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |

## <a name="see-also"></a>Vedere anche

[Interfacce Effects 11](d3d11-graphics-reference-effects11-interfaces.md)

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
