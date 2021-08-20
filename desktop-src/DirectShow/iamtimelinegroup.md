---
description: L'interfaccia IAMTimelineGroup imposta e recupera le proprietà sui gruppi in DirectShow Editing Services (DES). Un gruppo contiene una o più tracce ed eventualmente una o più composizione, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio. I gruppi sono le prime composizione in una sequenza temporale ed espongono anche l'interfaccia IAMTimelineComp. Una sequenza temporale può contenere più gruppi. Ogni gruppo ha gli attributi seguenti. Tipo di supporto associato. Frequenza dei fotogrammi con cui viene eseguito il rendering del gruppo, in fotogrammi al secondo (FPS). Tutte le modifiche vengono eseguite in un momento arrotondato al limite del frame più vicino, come definito dall'impostazione FPS del gruppo. Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI a due flussi video). Per creare un oggetto gruppo, chiamare IAMTimeline::CreateEmptyNode con il valore TIMELINE \_ MAJOR \_ TYPE \_ GROUP. È possibile eseguire una query sul puntatore IAMTimelineObj restituito per l'interfaccia IAMTimelineGroup.
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaccia IAMTimelineGroup (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9356e3edef0b61c119ec4cca774e9ec5976ac3732e0f0a508d103bc22bb0fef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155507"
---
# <a name="iamtimelinegroup-interface"></a>Interfaccia IAMTimelineGroup

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IAMTimelineGroup`L'interfaccia imposta e recupera le proprietà sui gruppi in DirectShow Editing [Services](directshow-editing-services.md) (DES).

Un gruppo contiene una o più tracce ed eventualmente una o più composizione, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio. I gruppi sono le prime composizione in una sequenza temporale ed espongono anche [**l'interfaccia IAMTimelineComp.**](iamtimelinecomp.md) Una sequenza temporale può contenere più gruppi.

Ogni gruppo ha gli attributi seguenti.

-   Tipo di supporto associato.
-   Frequenza dei fotogrammi con cui viene eseguito il rendering del gruppo, in fotogrammi al secondo (FPS). Tutte le modifiche vengono eseguite in un momento arrotondato al limite del frame più vicino, come definito dall'impostazione FPS del gruppo.
-   Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI a due flussi video).

Per creare un oggetto gruppo, chiamare [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con il valore TIMELINE \_ MAJOR TYPE \_ \_ GROUP. È possibile eseguire una query sul [**puntatore IAMTimelineObj restituito**](iamtimelineobj.md) per **l'interfaccia IAMTimelineGroup.**

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineGroup** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineGroup** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAMTimelineGroup** include questi metodi.



| Metodo                                                                            | Descrizione                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Non supportata.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Recupera il nome del gruppo definito dall'applicazione.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Recupera il tipo di supporto non compresso per il gruppo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera il numero di fotogrammi di cui è stato eseguito il rendering in anticipo durante l'anteprima.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera la frequenza dei fotogrammi di output di questo gruppo.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera la modalità di anteprima per il gruppo.<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | Recupera la priorità del gruppo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera il formato di compressione corrente per la ricocompressione intelligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Recupera la sequenza temporale a cui appartiene questo gruppo.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Non supportata.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina se per il gruppo è stato impostato un formato di compressione intelligente.<br/>                 |
| [**SetGroupName**](iamtimelinegroup-setgroupname.md)                             | Imposta il nome del gruppo definito dall'applicazione.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Imposta il tipo di supporto non compresso per il gruppo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Specifica il tipo di supporto del gruppo per i client di Automazione.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Specifica il numero di fotogrammi sottoposti a rendering in anticipo durante l'anteprima.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Imposta la modalità di anteprima per il gruppo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Imposta il formato di ricompressione video usando il formato di compressione di un file di origine.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Specifica un formato di compressione da usare per la ricocompressione intelligente.<br/>                       |
| [**SetTimeline**](iamtimelinegroup-settimeline.md)                               | Non supportata.<br/>                                                                       |



 

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



 

 
