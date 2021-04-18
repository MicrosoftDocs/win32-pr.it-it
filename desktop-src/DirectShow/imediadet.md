---
description: L'interfaccia IMediaDet recupera le informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la frequenza dei fotogrammi di ogni flusso.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interfaccia IMediaDet (qedit. h)
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
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325305"
---
# <a name="imediadet-interface"></a>Interfaccia IMediaDet

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IMediaDet` interfaccia recupera le informazioni su un file multimediale, ad esempio il numero di flussi e il tipo di supporto, la durata e la frequenza dei fotogrammi di ogni flusso. Contiene inoltre metodi per il recupero di singoli frame da un flusso video. L'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) espone questa interfaccia.

Per ottenere informazioni su un file usando questa interfaccia, seguire questa procedura:

1.  Creare un'istanza dell'oggetto MediaDet chiamando **CoCreateInstance**. L'ID di classe è CLSID \_ mediadet.
2.  Chiamare [**IMediaDet::p \_ nome file UT**](imediadet-put-filename.md) per specificare il nome del file di origine.
3.  Chiamare [**IMediaDet:: Get \_ OutputStreams**](imediadet-get-outputstreams.md) per ottenere il numero di flussi di output nell'origine.
4.  Chiamare [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) per specificare un determinato flusso.
5.  Chiamare uno dei metodi seguenti:
    -   [**IMediaDet:: Get \_ framerate**](imediadet-get-framerate.md)
    -   [**IMediaDet:: Get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet:: Get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet:: Get \_ StreamType**](imediadet-get-streamtype.md)

Per recuperare un frame video, chiamare [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md). Il frame restituito è sempre in formato RGB a 24 bit.

> [!Note]  
> Non usare lo stesso oggetto MediaDet con più file. Per ottenere informazioni o fotogrammi video da più di un file, usare istanze MediaDet separate.

 

L'interfaccia **IMediaDet** non supporta i formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , pertanto non è possibile usare questa interfaccia per ottenere campi interlacciati o informazioni sull'interlacciamento. Inoltre, se il decodificatore upstream supporta solo **VIDEOINFOHEADER2**, non è possibile utilizzare `IMediaDet` . Questo potrebbe essere il caso di un decodificatore MPEG-2, ad esempio. Inoltre, l' `IMediaDet` interfaccia ignora tutti i flussi nel file che non sono video o audio. Se, ad esempio, il file contiene un flusso audio, un flusso di dati e un flusso video, il metodo **get \_ OutputStreams** segnalerà solo due flussi (audio e video).

## <a name="members"></a>Membri

L'interfaccia **IMediaDet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaDet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMediaDet** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Passa il rilevatore di contenuti multimediali alla modalità di cattura della bitmap e cerca il grafico del filtro a un orario specificato.<br/> |
| [**ottenere \_ CurrentStream**](imediadet-get-currentstream.md)     | Recupera il numero di flusso attualmente utilizzato dal rilevamento multimediale.<br/>                               |
| [**Ottieni \_ nome file**](imediadet-get-filename.md)               | Recupera il nome del file di origine attualmente utilizzato dal rilevamento multimediale.<br/>                     |
| [**Ottieni \_ filtro**](imediadet-get-filter.md)                   | Recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.<br/>                  |
| [**Ottieni \_ framerate**](imediadet-get-framerate.md)             | Recupera la frequenza dei fotogrammi del flusso corrente.<br/>                                                 |
| [**ottenere \_ OutputStreams**](imediadet-get-outputstreams.md)     | Recupera il numero di flussi audio e video contenuti nell'origine multimediale.<br/>                  |
| [**ottenere \_ StreamLength**](imediadet-get-streamlength.md)       | Recupera la durata del flusso corrente.<br/>                                                   |
| [**ottenere \_ StreamMediaType**](imediadet-get-streammediatype.md) | Recupera il tipo di supporto del flusso corrente.<br/>                                                 |
| [**ottenere \_ StreamType**](imediadet-get-streamtype.md)           | Recupera l'identificatore univoco globale (GUID) per il tipo di supporto del flusso corrente.<br/>       |
| [**ottenere \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Recupera una stringa che rappresenta il GUID del tipo di supporto per il flusso corrente.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Recupera un frame video al momento del supporto specificato.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Recupera un puntatore all'interfaccia [**ISampleGrabber**](isamplegrabber.md) .<br/>                  |
| [**Inserisci \_ CurrentStream**](imediadet-put-currentstream.md)     | Specifica il numero di flusso per il rilevatore multimediale da usare.<br/>                                      |
| [**Inserisci \_ nome file**](imediadet-put-filename.md)               | Specifica il nome del file di origine per il rilevatore multimediale da usare.<br/>                            |
| [**Inserisci \_ filtro**](imediadet-put-filter.md)                   | Specifica un filtro di origine per il rilevatore di contenuti multimediali da usare.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Recupera un frame video nel tempo di supporto specificato e lo scrive in un file.<br/>                    |



 

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



 

 
