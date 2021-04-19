---
description: "L'interfaccia IRenderEngine esegue il rendering di un progetto di servizi di modifica DirectShow (DES) costruendo un grafico di filtro da una sequenza temporale. DES fornisce due componenti che implementano questa interfaccia: il motore di rendering di base crea output non compresso."
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaccia IRenderEngine (qedit. h)
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
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332576"
---
# <a name="irenderengine-interface"></a>Interfaccia IRenderEngine

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IRenderEngine` interfaccia esegue il rendering di un progetto di [servizi di modifica DirectShow](directshow-editing-services.md) (des) costruendo un grafico di filtro da una sequenza temporale.

DES fornisce due componenti che implementano questa interfaccia:

-   Il *motore di rendering di base* crea output non compresso. È possibile usare l'output per l'anteprima oppure instradarlo tramite filtri di compressione e scriverlo in un file.
-   Il *motore di rendering intelligente* crea l'output compresso, usando la *ricompressione intelligente*. Con la ricompressione intelligente, un file di origine viene ricompresso solo se il formato è diverso dal formato di output. Un'origine con un formato corrispondente viene scritta direttamente nel file di output. A seconda dello scenario, la ricompressione intelligente può migliorare significativamente il tempo di rendering.

Il motore di rendering intelligente supporta anche l'interfaccia [**ISmartRenderEngine**](ismartrenderengine.md) .

Sebbene un'applicazione possa creare un grafico di filtro e passarlo a un motore di rendering, lo scenario tipico è che il motore di rendering crei il grafico dei filtri. La compilazione del grafo è un processo in due fasi. Per prima cosa, compilare il front-end chiamando il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) . Connettere quindi i pin di output sul front-end ai filtri di rendering desiderati:

-   Renderer video e audio per l'anteprima
-   Compresser, multiplexer e writer di file per generare l'output finale.

## <a name="members"></a>Membri

L'interfaccia **IRenderEngine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IRenderEngine** dispone di questi metodi.



| Metodo                                                                             | Descrizione                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Commit**](irenderengine-commit.md)                                             | Non implementato.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Compila il front-end del grafico di filtro dalla sequenza temporale corrente.<br/>        |
| [**Liberare**](irenderengine-decommit.md)                                         | Non implementato.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | Non supportata.<br/>                                                             |
| [**Getcaps**](irenderengine-getcaps.md)                                           | Non implementato.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Recupera il grafico di filtro creato dal motore di rendering, se disponibile.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Recupera il pin di output per il gruppo specificato.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Recupera la sequenza temporale attualmente utilizzata dal motore di rendering.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Recupera la stringa del fornitore.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Crea la parte in anteprima del grafico del filtro.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Elimina il grafico di filtro del motore di rendering e tutti gli oggetti associati.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Imposta il livello di riconnessione dinamica durante il rendering.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Specifica un grafico di filtro per il motore di rendering da usare.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | Non supportata.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Non supportata.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Imposta l'intervallo di tempo di cui eseguire il rendering.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Imposta l'intervallo di tempo di cui eseguire il rendering, come **valore Double**.<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | Non supportata.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Specifica il modo in cui il motore di rendering convalida i nomi di file.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Imposta la sequenza temporale per il motore di rendering da utilizzare.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | Non supportata.<br/>                                                             |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 
