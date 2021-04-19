---
description: L'interfaccia IAMTimelineTrack fornisce metodi per la modifica degli oggetti Track nei servizi di modifica DirectShow (DES). Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interfaccia IAMTimelineTrack (qedit. h)
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
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333267"
---
# <a name="iamtimelinetrack-interface"></a>Interfaccia IAMTimelineTrack

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineTrack` interfaccia fornisce metodi per la modifica degli oggetti *Track* nei [servizi di modifica DirectShow](directshow-editing-services.md) (des).

Una traccia contiene un elenco di origini di cui viene eseguito il rendering nell'output finale. Le origini all'interno della stessa traccia potrebbero non sovrapporsi. Le tracce video possono avere sia effetti che transizioni. Il motore di rendering applica gli effetti prima di applicare le transizioni. Le tracce audio possono avere effetti, ma non transizioni. Per ulteriori informazioni, vedere [il modello di sequenza temporale](the-timeline-model.md).

Per creare un oggetto Track, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con il tipo di sequenza temporale del valore \_ principale \_ \_ Track. È possibile eseguire una query sul puntatore **IAMTimelineObj** restituito per l' `IAMTimelineTrack` interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineTrack** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrack** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineTrack** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Determina se la traccia è vuota (non contiene oggetti di origine).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Esegue la ricerca della successiva origine visualizzata all'ora specificata o successiva.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Esegue la ricerca della successiva origine visualizzata nell'ora specificata o in una versione successiva, con l'oggetto specificato come valore [**REFTIME**](reftime.md) .<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Recupera l'origine successiva dopo l'origine specificata.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Recupera il numero di origini nella traccia.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Recupera l'oggetto di origine più vicino al tempo specificato, dato come valore [**REFTIME**](reftime.md) .<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi, usando i valori [**REFTIME**](reftime.md) .<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Non supportata.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Non supportata.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Aggiunge un'origine alla traccia.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Rimuove tutti gli elementi dalla traccia tra le ore specificate.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Rimuove tutti gli elementi dalla traccia tra gli orari specificati, specificati come valori [**REFTIME**](reftime.md) .<br/>                                |



 

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



 

 
