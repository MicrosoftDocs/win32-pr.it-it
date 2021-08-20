---
description: L'interfaccia IAMTimelineComp inserisce o recupera tracce virtuali in una composizione in DirectShow Editing Services (DES). Una composizione è una raccolta di livelli che funge da singola traccia composita.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interfaccia IAMTimelineComp (Qedit.h)
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
ms.openlocfilehash: d1531d743bb705c20473568d9619aae804e47996244d36906fcb482404ee833b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999247"
---
# <a name="iamtimelinecomp-interface"></a>Interfaccia IAMTimelineComp

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

**L'interfaccia IAMTimelineComp** inserisce o recupera tracce virtuali in una composizione in [DirectShow Editing Services](directshow-editing-services.md) (DES).

Una composizione è una raccolta di livelli che funge da singola traccia *composita.* Ad esempio, una composizione che contiene due tracce con una transizione tra di esse funge da singola traccia con la transizione precomposa. Una composizione deve contenere elementi multimediali di un solo tipo (ad esempio audio o video), ma questa limitazione non viene applicata. Una *traccia virtuale* è qualsiasi oggetto che può risiedere in una composizione, incluse tracce e altre composizione.

I nodi più in alto nella sequenza temporale sono *i gruppi*. I gruppi implementano sia `IAMTimelineComp` l'interfaccia che [**l'interfaccia IAMTimelineGroup.**](iamtimelinegroup.md)

Per creare un oggetto di composizione, chiamare [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con il valore TIMELINE \_ MAJOR TYPE \_ \_ COMPOSITE. È possibile eseguire una query sul puntatore [**IAMTimelineObj restituito**](iamtimelineobj.md) per `IAMTimelineComp` l'interfaccia. Per altre informazioni, vedere [Modello di sequenza temporale](the-timeline-model.md) e Costruzione di una sequenza [temporale.](constructing-a-timeline.md)

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineComp** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineComp** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAMTimelineComp** include questi metodi.



| Metodo                                                                       | Descrizione                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCountOfType**](iamtimelinecomp-getcountoftype.md)                     | Recupera in modo ricorsivo il numero di oggetti di un determinato tipo contenuto in questa composizione e in tutte le relative tracce virtuali.<br/>                      |
| [**GetNextVTrack**](iamtimelinecomp-getnextvtrack.md)                       | Recupera la traccia virtuale successiva dopo una traccia virtuale specificata.<br/>                                                                              |
| [**GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md)   | Esegue un ordinamento depth-first delle tracce virtuali contenute in questa composizione e recupera *l'ennesimo* traccia virtuale da tale ordinamento.<br/> |
| [**GetRecursiveLayerOfTypeI**](iamtimelinecomp-getrecursivelayeroftypei.md) | Non supportata.<br/>                                                                                                                                 |
| [**GetVTrack**](iamtimelinecomp-getvtrack.md)                               | Recupera la traccia virtuale con la priorità specificata.<br/>                                                                                         |
| [**VTrackGetCount**](iamtimelinecomp-vtrackgetcount.md)                     | Recupera il numero di tracce virtuali contenute nella composizione.<br/>                                                                           |
| [**VTrackInsBefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Inserisce una traccia virtuale nella composizione con la priorità specificata.<br/>                                                                        |
| [**VTrackSwapPriorities**](iamtimelinecomp-vtrackswappriorities.md)         | Cambia i livelli di priorità di due tracce.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
