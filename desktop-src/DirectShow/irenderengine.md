---
description: "L'interfaccia IRenderEngine esegue il rendering di DirectShow di servizi di modifica (DES) creando un grafico di filtro da una sequenza temporale. DES fornisce due componenti che implementano questa interfaccia: il motore di rendering di base crea un output non compresso."
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaccia IRenderEngine (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051311"
---
# <a name="irenderengine-interface"></a>Interfaccia IRenderEngine

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia esegue il rendering di DirectShow di servizi di modifica (DES) creando un grafico `IRenderEngine` di filtro da una sequenza temporale. [](directshow-editing-services.md)

DES fornisce due componenti che implementano questa interfaccia:

-   Il *motore di rendering di base* crea un output non compresso. È possibile usare l'output per l'anteprima o instradare l'output tramite filtri di compressione e scriverlo in un file.
-   Il *motore di rendering intelligente* crea un output compresso usando la *ricompressione intelligente.* Con la ricompressione intelligente, un file di origine viene compresso nuovamente solo se il formato è diverso dal formato di output. Un'origine con un formato corrispondente viene scritta direttamente nel file di output. A seconda dello scenario, la ricompressione intelligente può migliorare notevolmente il tempo di rendering.

Il motore di rendering intelligente supporta anche [**l'interfaccia ISmartRenderEngine.**](ismartrenderengine.md)

Anche se un'applicazione può creare un grafo di filtro e passarlo a un motore di rendering, lo scenario tipico è che il motore di rendering crei il grafico dei filtri. La compilazione del grafo è un processo in due fasi. Prima di tutto, compilare il front-end chiamando il [**metodo IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md) Connettere quindi i pin di output sul front-end ai filtri di rendering desiderati:

-   Renderer video e audio per l'anteprima o
-   Compressori, multiplexer e writer di file per generare l'output finale.

## <a name="members"></a>Membri

**L'interfaccia IRenderEngine** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IRenderEngine** include questi metodi.



| Metodo                                                                             | Descrizione                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Commettere**](irenderengine-commit.md)                                             | Non implementato.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Compila il front-end del grafico dei filtri dalla sequenza temporale corrente.<br/>        |
| [**Decommit**](irenderengine-decommit.md)                                         | Non implementato.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | Non supportata.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Non implementato.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Recupera il grafico di filtro costruito dal motore di rendering, se presente.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Recupera il pin di output per il gruppo specificato.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Recupera la sequenza temporale attualmente in uso dal motore di rendering.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Recupera la stringa del fornitore.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Crea la parte di anteprima del grafico dei filtri.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Rimuove il grafico dei filtri del motore di rendering e tutti gli oggetti associati.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Imposta il livello di riconnessione dinamica durante il rendering.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Specifica un grafo di filtro da usare per il motore di rendering.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | Non supportata.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Non supportata.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Imposta l'intervallo di tempo di cui eseguire il rendering.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Imposta l'intervallo di tempo di cui eseguire il rendering, come **valore double.**<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | Non supportata.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Specifica il modo in cui il motore di rendering convalida i nomi di file.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Imposta la sequenza temporale da usare per il motore di rendering.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | Non supportata.<br/>                                                             |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> </dl>

 

 
