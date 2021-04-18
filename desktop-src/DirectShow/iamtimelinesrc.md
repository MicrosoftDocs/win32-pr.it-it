---
description: L'interfaccia IAMTimelineSrc fornisce metodi per la modifica e l'impostazione delle proprietà negli oggetti di origine nei servizi di modifica DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaccia IAMTimelineSrc (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325178"
---
# <a name="iamtimelinesrc-interface"></a>Interfaccia IAMTimelineSrc

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineSrc` interfaccia fornisce metodi per la modifica e l'impostazione delle proprietà negli oggetti di origine nei [servizi di modifica DirectShow](directshow-editing-services.md) (des). Un oggetto di origine rappresenta un flusso da un'origine multimediale.

È possibile usare una parte dei dati all'interno di un file di origine impostando gli orari di inizio e di fine del supporto. Questi valori specificano l'inizio e la fine dell'oggetto di origine rispetto all'origine del supporto originale. I tempi del supporto possono differire dall'ora di inizio e di fine dell'oggetto nella sequenza temporale, consentendo la riproduzione veloce o lenta. (Con le origini audio, viene eseguito il pitch shift).

Per creare un oggetto di origine, chiamare [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con l' \_ origine del tipo principale della sequenza temporale del valore \_ \_ . È possibile eseguire una query sul puntatore [**IAMTimelineObj**](iamtimelineobj.md) restituito per l'interfaccia **IAMTimelineSrc** . Per ulteriori informazioni, vedere [creazione di una sequenza temporale](constructing-a-timeline.md) e [utilizzo di origini](working-with-sources.md).

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineSrc** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSrc** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineSrc** dispone di questi metodi.



| Metodo                                                    | Descrizione                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Arrotonda i valori temporali specificati al limite del frame più vicino.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Arrotonda i valori temporali specificati, specificati come valori **REFTIME** , al limite di frame più vicino.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Recupera la lunghezza del supporto di questo oggetto di origine.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Recupera la lunghezza del supporto di questo oggetto di origine, come valore **REFTIME** .<br/>                     |
| [**Getmedianame**](iamtimelinesrc-getmedianame.md)       | Recupera il nome del file di origine rappresentato da questo oggetto di origine.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Recupera l'ora di inizio e di fine del supporto.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Recupera le ore di inizio e di fine del supporto, come valori **REFTIME** .<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Recupera il numero corrente del flusso per l'oggetto di origine.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Recupera la modalità di estensione di un'origine video.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indica se il clip viene riprodotto alla frequenza di riproduzione normale.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Imposta l'ora di arresto, relativa alla sequenza temporale.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Imposta l'ora di arresto, come valore di **REFTIME** .<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Specifica la durata del file di origine.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Specifica la durata del file di origine, come valore **REFTIME** .<br/>                            |
| [**MEDIANAME**](iamtimelinesrc-setmedianame.md)       | Specifica il nome del file di origine rappresentato da questo oggetto di origine.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Imposta l'ora di inizio e di fine del supporto.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Imposta l'ora di inizio e di fine del supporto, come valori **REFTIME** .<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Imposta la modalità di estensione di un'origine video.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Unisce questo oggetto di origine a un altro oggetto di origine.<br/>                                            |



 

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



 

 
