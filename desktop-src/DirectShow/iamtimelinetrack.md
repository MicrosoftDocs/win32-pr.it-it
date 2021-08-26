---
description: L'interfaccia IAMTimelineTrack fornisce metodi per la modifica di oggetti traccia in DirectShow Editing Services (DES). Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaccia IAMTimelineTrack (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cc33facc22023d6e93c8dcfa3804d111d9c99f49be16d8271b09a7bf938b49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965081"
---
# <a name="iamtimelinetrack-interface"></a>Interfaccia IAMTimelineTrack

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IAMTimelineTrack`L'interfaccia fornisce metodi per la modifica di *oggetti* traccia in DirectShow [Editing Services](directshow-editing-services.md) (DES).

Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale. Le origini all'interno della stessa traccia potrebbero non sovrapporsi. Le tracce video possono avere effetti e transizioni. Il motore di rendering applica gli effetti prima di applicare le transizioni. Le tracce audio possono avere effetti, ma non transizioni. Per altre informazioni, vedere [Modello di sequenza temporale.](the-timeline-model.md)

Per creare un oggetto traccia, chiamare [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con il valore TIMELINE \_ MAJOR TYPE \_ \_ TRACK. È possibile eseguire una query sul puntatore **IAMTimelineObj restituito** per `IAMTimelineTrack` l'interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineTrack** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrack** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IAMTimelineTrack** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina se la traccia è vuota (non contiene oggetti di origine).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Cerca nella traccia l'origine successiva visualizzata all'ora specificata o in un secondo momento.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Cerca nella traccia l'origine successiva visualizzata all'ora specificata o successiva, con l'oggetto specificato come [**valore REFTIME.**](reftime.md)<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera l'origine successiva all'origine specificata.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera il numero di origini nella traccia.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera l'oggetto di origine più vicino all'ora specificata, in base alle condizioni limite specificate.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera l'oggetto di origine più vicino all'ora specificata, dato come [**valore REFTIME.**](reftime.md)<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Divide tutti gli oggetti esistenti all'ora specificata e inserisce uno spazio tra di essi.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Divide tutti gli oggetti esistenti all'ora specificata e inserisce uno spazio tra di essi, usando [**i valori REFTIME.**](reftime.md)<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Non supportata.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Non supportata.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Aggiunge un'origine alla traccia.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Rimuove tutti gli elementi dalla traccia tra gli orari specificati.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Rimuove tutti gli elementi dalla traccia tra gli orari specificati, specificati come [**valori REFTIME.**](reftime.md)<br/>                                |



 

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



 

 
