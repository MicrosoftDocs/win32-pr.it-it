---
description: L'interfaccia IMediaDet recupera informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la frequenza dei fotogrammi di ogni flusso.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaccia IMediaDet (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abdf913ab74e6f0f988449a14b84b5be109b9380ebbfb2473edd4a9980f3c577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819033"
---
# <a name="imediadet-interface"></a>Interfaccia IMediaDet

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia recupera informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la `IMediaDet` frequenza dei fotogrammi di ogni flusso. Contiene anche metodi per recuperare singoli fotogrammi da un flusso video. [L'oggetto Media Detector (MediaDet)](media-detector--mediadet.md) espone questa interfaccia.

Per ottenere informazioni su un file tramite questa interfaccia, seguire questa procedura:

1.  Creare un'istanza dell'oggetto MediaDet chiamando **CoCreateInstance**. L'ID classe è CLSID \_ MediaDet.
2.  Chiamare [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) per specificare il nome del file di origine.
3.  Chiamare [**IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) per ottenere il numero di flussi di output nell'origine.
4.  Chiamare [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md) per specificare un flusso specifico.
5.  Chiamare uno dei metodi seguenti:
    -   [**IMediaDet::get \_ FrameRate**](imediadet-get-framerate.md)
    -   [**IMediaDet::get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet::get \_ StreamType**](imediadet-get-streamtype.md)

Per recuperare un fotogramma video, chiamare [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md). Il frame restituito è sempre in formato RGB a 24 bit.

> [!Note]  
> Non usare lo stesso oggetto MediaDet con più file. Per ottenere informazioni o fotogrammi video da più file, usare istanze di MediaDet separate.

 

**L'interfaccia IMediaDet** non supporta i formati [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) pertanto non è possibile usare questa interfaccia per ottenere campi interlacciati o informazioni sull'interlacciamento. Inoltre, se il decodificatore upstream supporta solo **VIDEOINFOHEADER2,** non è possibile usare `IMediaDet` . Questo potrebbe essere il caso di un decodificatore MPEG-2, ad esempio. Inoltre, `IMediaDet` l'interfaccia ignora tutti i flussi nel file che non sono video o audio. Ad esempio, se il file contiene un flusso audio, un flusso di dati e un flusso video, il metodo **get \_ OutputStreams** segnalerà solo due flussi (audio e video).

## <a name="members"></a>Membri

**L'interfaccia IMediaDet** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMediaDet** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IMediaDet.**



| Metodo                                                        | Descrizione                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Passa il rilevatore multimediale alla modalità di cattura bitmap e cerca il grafico dei filtri a un'ora specificata.<br/> |
| [**get \_ CurrentStream**](imediadet-get-currentstream.md)     | Recupera il numero di flusso attualmente usato dal rilevatore di supporti.<br/>                               |
| [**get \_ Filename**](imediadet-get-filename.md)               | Recupera il nome del file di origine attualmente usato dal rilevatore di supporti.<br/>                     |
| [**get \_ filter**](imediadet-get-filter.md)                   | Recupera un puntatore al filtro di origine attualmente usato dal rilevatore di supporti.<br/>                  |
| [**get \_ FrameRate**](imediadet-get-framerate.md)             | Recupera la frequenza dei fotogrammi del flusso corrente.<br/>                                                 |
| [**get \_ OutputStreams**](imediadet-get-outputstreams.md)     | Recupera il numero di flussi audio e video contenuti nell'origine multimediale.<br/>                  |
| [**get \_ StreamLength**](imediadet-get-streamlength.md)       | Recupera la durata del flusso corrente.<br/>                                                   |
| [**get \_ StreamMediaType**](imediadet-get-streammediatype.md) | Recupera il tipo di supporto del flusso corrente.<br/>                                                 |
| [**get \_ StreamType**](imediadet-get-streamtype.md)           | Recupera l'identificatore univoco globale (GUID) per il tipo di supporto del flusso corrente.<br/>       |
| [**get \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Recupera una stringa che rappresenta il GUID del tipo di supporto per il flusso corrente.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Recupera un fotogramma video all'ora del supporto specificata.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Recupera un puntatore [**all'interfaccia ISampleGrabber.**](isamplegrabber.md)<br/>                  |
| [**put \_ CurrentStream**](imediadet-put-currentstream.md)     | Specifica il numero di flusso da usare per il rilevamento multimediale.<br/>                                      |
| [**Put \_ Filename**](imediadet-put-filename.md)               | Specifica il nome del file di origine da usare per il rilevamento multimediale.<br/>                            |
| [**Put \_ Filter**](imediadet-put-filter.md)                   | Specifica un filtro di origine per il rilevamento multimediale da usare.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Recupera un fotogramma video all'ora del supporto specificata e lo scrive in un file.<br/>                    |



 

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



 

 
