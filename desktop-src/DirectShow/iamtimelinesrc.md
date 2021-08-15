---
description: L'interfaccia IAMTimelineSrc fornisce metodi per la modifica e l'impostazione delle proprietà sugli oggetti di origine in DirectShow Editing Services (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interfaccia IAMTimelineSrc (Qedit.h)
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
ms.openlocfilehash: 5d2ad5684df6298bde458e87ff322b21622139930fa9aaf994fda0e7ba7e987e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399198"
---
# <a name="iamtimelinesrc-interface"></a>Interfaccia IAMTimelineSrc

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia fornisce metodi per la modifica e l'impostazione delle proprietà sugli oggetti di origine `IAMTimelineSrc` in DirectShow Editing [Services](directshow-editing-services.md) (DES). Un oggetto di origine rappresenta un flusso da un'origine multimediale.

È possibile usare una parte dei dati all'interno di un file di origine impostando i tempi di avvio e arresto dei supporti. Questi valori specificano l'inizio e la fine dell'oggetto di origine, rispetto all'origine multimediale originale. I tempi multimediali possono differire dai tempi di avvio e arresto dell'oggetto nella sequenza temporale, consentendo la riproduzione veloce o lenta. Con le origini audio, si verifica lo spostamento del passo.

Per creare un oggetto di origine, chiamare [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con il valore TIMELINE \_ MAJOR TYPE \_ \_ SOURCE. È possibile eseguire una query sul puntatore [**IAMTimelineObj restituito**](iamtimelineobj.md) per **l'interfaccia IAMTimelineSrc.** Per altre informazioni, vedere [Costruzione di una](constructing-a-timeline.md) sequenza temporale e Uso delle [origini](working-with-sources.md).

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineSrc** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSrc** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMTimelineSrc.**



| Metodo                                                    | Descrizione                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)     | Arrotonda i valori di ora specificati al limite del frame più vicino.<br/>                               |
| [**FixMediaTimes2**](iamtimelinesrc-fixmediatimes2.md)   | Arrotonda i valori di ora specificati, specificati come **valori REFTIME,** al limite del frame più vicino.<br/> |
| [**GetDefaultFPS**](iamtimelinesrc-getdefaultfps.md)     | Recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine.<br/>                                             |
| [**GetMediaLength**](iamtimelinesrc-getmedialength.md)   | Recupera la lunghezza del supporto di questo oggetto di origine.<br/>                                             |
| [**GetMediaLength2**](iamtimelinesrc-getmedialength2.md) | Recupera la lunghezza dei supporti di questo oggetto di origine, come **valore REFTIME.**<br/>                     |
| [**GetMediaName**](iamtimelinesrc-getmedianame.md)       | Recupera il nome del file di origine rappresentato da questo oggetto di origine.<br/>                      |
| [**GetMediaTimes**](iamtimelinesrc-getmediatimes.md)     | Recupera i tempi di avvio e arresto dei supporti.<br/>                                                     |
| [**GetMediaTimes2**](iamtimelinesrc-getmediatimes2.md)   | Recupera i tempi di avvio e arresto dei supporti, come **valori REFTIME.**<br/>                              |
| [**GetStreamNumber**](iamtimelinesrc-getstreamnumber.md) | Recupera il numero di flusso corrente per l'oggetto di origine.<br/>                                    |
| [**GetStretchMode**](iamtimelinesrc-getstretchmode.md)   | Recupera la modalità di estensione di un'origine video.<br/>                                                 |
| [**IsNormalRate**](iamtimelinesrc-isnormalrate.md)       | Indica se il clip verrà riprodotto alla velocità di riproduzione normale.<br/>                             |
| [**ModifyStopTime**](iamtimelinesrc-modifystoptime.md)   | Imposta l'ora di arresto, relativa alla sequenza temporale.<br/>                                                 |
| [**ModifyStopTime2**](iamtimelinesrc-modifystoptime2.md) | Imposta l'ora di arresto come **valore REFTIME.**<br/>                                                   |
| [**SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)     | Imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.<br/>                                                  |
| [**SetMediaLength**](iamtimelinesrc-setmedialength.md)   | Specifica la durata del file di origine.<br/>                                                    |
| [**SetMediaLength2**](iamtimelinesrc-setmedialength2.md) | Specifica la durata del file di origine, come **valore REFTIME.**<br/>                            |
| [**SetMediaName**](iamtimelinesrc-setmedianame.md)       | Specifica il nome del file di origine rappresentato da questo oggetto di origine.<br/>                      |
| [**SetMediaTimes**](iamtimelinesrc-setmediatimes.md)     | Imposta le ore di arresto e avvio del supporto.<br/>                                                          |
| [**SetMediaTimes2**](iamtimelinesrc-setmediatimes2.md)   | Imposta le ore di arresto e avvio dei supporti, come **valori REFTIME.**<br/>                                   |
| [**SetStreamNumber**](iamtimelinesrc-setstreamnumber.md) | Specifica il flusso da leggere dal file di origine associato a questo oggetto di origine.<br/>       |
| [**SetStretchMode**](iamtimelinesrc-setstretchmode.md)   | Imposta la modalità di estensione di un'origine video.<br/>                                                      |
| [**SpliceWithNext**](iamtimelinesrc-splicewithnext.md)   | Unisce questo oggetto di origine a un altro oggetto di origine.<br/>                                            |



 

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



 

 
