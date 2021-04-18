---
description: L'interfaccia IAMTimelineComp inserisce o recupera tracce virtuali in una composizione in servizi di modifica DirectShow (DES). Una composizione è una raccolta di livelli che funge da singolo tracciato composito.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaccia IAMTimelineComp (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333705"
---
# <a name="iamtimelinecomp-interface"></a>Interfaccia IAMTimelineComp

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'interfaccia **IAMTimelineComp** inserisce o recupera tracce virtuali in una composizione in [servizi di modifica DirectShow](directshow-editing-services.md) (des).

Una composizione è una raccolta di livelli che funge da singolo *tracciato* composito. Ad esempio, una composizione che contiene due tracce con una transizione tra loro funge da singola traccia con la transizione precomposita. Una composizione deve contenere supporti di un solo tipo, ad esempio audio o video, ma questa limitazione non viene applicata. Una *traccia virtuale* è qualsiasi oggetto che può risiedere in una composizione, incluse le tracce e altre composizioni.

I nodi più in alto nella sequenza temporale sono *gruppi*. I gruppi implementano sia l'interfaccia `IAMTimelineComp` che l'interfaccia [**IAMTimelineGroup**](iamtimelinegroup.md) .

Per creare un oggetto Composition, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il tipo principale della sequenza temporale del valore \_ \_ \_ composito. È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l' `IAMTimelineComp` interfaccia. Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md) e [creazione di una sequenza temporale](constructing-a-timeline.md).

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineComp** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineComp** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineComp** dispone di questi metodi.



| Metodo                                                                       | Descrizione                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Recupera il numero di oggetti di un tipo specificato contenuto nella composizione e in tutte le relative tracce virtuali, in modo ricorsivo.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Recupera la traccia virtuale successiva dopo una traccia virtuale specificata.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Esegue un ordine di profondità-primo delle tracce virtuali contenute in questa composizione e recupera la traccia virtuale *n* dall'ordinamento.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | Non supportata.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Recupera la traccia virtuale alla priorità specificata.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Recupera il numero di tracce virtuali contenute nella composizione.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Inserisce una traccia virtuale nella composizione con la priorità specificata.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Passa i livelli di priorità di due tracce.<br/>                                                                                                    |



 

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



 

 
