---
description: "L'interfaccia IAMTimelineGroup imposta e recupera le proprietà sui gruppi in servizi di modifica DirectShow (DES). Un gruppo contiene una o più tracce e possibilmente una o più composizioni, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio. I gruppi sono le composizioni più in alto in una sequenza temporale ed espongono anche l'interfaccia IAMTimelineComp. Una sequenza temporale può contenere più gruppi. Ogni gruppo ha gli attributi seguenti. Tipo di supporto associato. Frequenza dei fotogrammi a cui viene eseguito il rendering del gruppo, in frame al secondo (FPS). Tutte le modifiche vengono eseguite in un momento arrotondato al limite di frame più vicino, come definito dall'impostazione FPS del gruppo. Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI con due flussi video). Per creare un oggetto gruppo, chiamare IAMTimeline:: CreateEmptyNode con il gruppo di tipi principali della sequenza temporale del valore \\_ \\_ \\_ . È possibile eseguire una query sul puntatore IAMTimelineObj restituito per l'interfaccia IAMTimelineGroup."
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interfaccia IAMTimelineGroup (qedit. h)
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
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333597"
---
# <a name="iamtimelinegroup-interface"></a>Interfaccia IAMTimelineGroup

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineGroup` interfaccia imposta e recupera le proprietà sui gruppi in [servizi di modifica DirectShow](directshow-editing-services.md) (des).

Un gruppo contiene una o più tracce e possibilmente una o più composizioni, che a loro volta contengono clip di origine di un tipo uniforme, ad esempio video o audio. I gruppi sono le composizioni più in alto in una sequenza temporale ed espongono anche l'interfaccia [**IAMTimelineComp**](iamtimelinecomp.md) . Una sequenza temporale può contenere più gruppi.

Ogni gruppo ha gli attributi seguenti.

-   Tipo di supporto associato.
-   Frequenza dei fotogrammi a cui viene eseguito il rendering del gruppo, in frame al secondo (FPS). Tutte le modifiche vengono eseguite in un momento arrotondato al limite di frame più vicino, come definito dall'impostazione FPS del gruppo.
-   Un livello di priorità, per la scrittura di file con più flussi dello stesso tipo di supporto (ad esempio, un file AVI con due flussi video).

Per creare un oggetto gruppo, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il gruppo di tipi principali della sequenza temporale del valore \_ \_ \_ . È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l'interfaccia **IAMTimelineGroup** .

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineGroup** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineGroup** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineGroup** dispone di questi metodi.



| Metodo                                                                            | Descrizione                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**ClearRecompressFormatDirty**](iamtimelinegroup-clearrecompressformatdirty.md) | Non supportata.<br/>                                                                       |
| [**GetGroupName**](iamtimelinegroup-getgroupname.md)                             | Recupera il nome definito dall'applicazione del gruppo.<br/>                                 |
| [**GetMediaType**](iamtimelinegroup-getmediatype.md)                             | Recupera il tipo di supporto non compresso per il gruppo.<br/>                                 |
| [**GetOutputBuffering**](iamtimelinegroup-getoutputbuffering.md)                 | Recupera il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.<br/>                   |
| [**GetOutputFPS**](iamtimelinegroup-getoutputfps.md)                             | Recupera la frequenza dei fotogrammi di output di questo gruppo.<br/>                                       |
| [**GetPreviewMode**](iamtimelinegroup-getpreviewmode.md)                         | Recupera la modalità di anteprima per il gruppo.<br/>                                            |
| [**GetPriority**](iamtimelinegroup-getpriority.md)                               | Recupera la priorità del gruppo.<br/>                                                      |
| [**GetSmartRecompressFormat**](iamtimelinegroup-getsmartrecompressformat.md)     | Recupera il formato di compressione corrente per la ricompressione intelligente.<br/>                    |
| [**GetTimeline**](iamtimelinegroup-gettimeline.md)                               | Recupera la sequenza temporale a cui appartiene il gruppo.<br/>                                  |
| [**IsRecompressFormatDirty**](iamtimelinegroup-isrecompressformatdirty.md)       | Non supportata.<br/>                                                                       |
| [**IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) | Determina se è stato impostato un formato di compressione intelligente per il gruppo.<br/>                 |
| [**Segroupname**](iamtimelinegroup-setgroupname.md)                             | Imposta il nome definito dall'applicazione del gruppo.<br/>                                      |
| [**SetMediaType**](iamtimelinegroup-setmediatype.md)                             | Imposta il tipo di supporto non compresso per il gruppo.<br/>                                      |
| [**SetMediaTypeForVB**](iamtimelinegroup-setmediatypeforvb.md)                   | Specifica il tipo di supporto di gruppo per i client di automazione.<br/>                              |
| [**SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)                 | Specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.<br/>                   |
| [**SetOutputFPS**](iamtimelinegroup-setoutputfps.md)                             | Imposta la frequenza dei fotogrammi di output non compressi per questo gruppo.<br/>                              |
| [**SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)                         | Imposta la modalità di anteprima per il gruppo.<br/>                                                 |
| [**SetRecompFormatFromSource**](iamtimelinegroup-setrecompformatfromsource.md)   | Imposta il formato di ricompressione video usando il formato di compressione da un file di origine.<br/> |
| [**SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)     | Specifica un formato di compressione da utilizzare per la ricompressione intelligente.<br/>                       |
| [**Sequenza temporale**](iamtimelinegroup-settimeline.md)                               | Non supportata.<br/>                                                                       |



 

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



 

 
