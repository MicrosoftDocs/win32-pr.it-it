---
description: Le funzioni di Network Monitor, elencate nella tabella seguente, possono essere utilizzate per sviluppare parser o esperti.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Funzioni comuni di esperti e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305956"
---
# <a name="expert-and-parser-common-functions"></a>Funzioni comuni di esperti e parser

Le funzioni di Network Monitor, elencate nella tabella seguente, possono essere utilizzate per sviluppare [*parser*](p.md) o [*esperti*](e.md).



| Funzione                                                               | Descrizione                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | Confronta due indirizzi specificati.                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | Confronta un determinato indirizzo con l'indirizzo di destinazione di un frame.                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | Confronta un determinato indirizzo con l'indirizzo di origine di un frame.                          |
| [FilterAddObject](filteraddobject.md)                                 | Aggiunge un singolo oggetto a un filtro.                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | Trova la prima istanza di una determinata proprietà.                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | Trova l'istanza successiva di una determinata proprietà.                                        |
| [GetCaptureComment](getcapturecomment.md)                             | Recupera il commento di un'acquisizione.                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | Recupera il commento di un'acquisizione dal relativo file di acquisizione.                           |
| [GetCaptureMacType](getcapturemactype.md)                             | Recupera il tipo MAC dell'acquisizione.                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | Recupera l'indicatore di timeout di acquisizione.                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | Recupera i frame totali nell'acquisizione.                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | Recupera un elenco di tutti i protocolli contrassegnati come abilitati.                            |
| [GetFrame](getframe.md)                                               | Recupera un handle per un frame specificato.                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | Recupera un handle per una determinata acquisizione.                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | Recupera l'offset dell'indirizzo di destinazione per un frame specificato.                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | Recupera un frame per un handle di frame specificato.                                         |
| [GetFrameLength](getframelength.md)                                   | Recupera la lunghezza di un frame specificato.                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | Recupera la lunghezza dell'intestazione MAC per un frame specificato.                           |
| [GetFrameMacType](getframemactype.md)                                 | Recupera il tipo MAC per un frame specificato.                                           |
| [GetFrameNumber](getframenumber.md)                                   | Restituisce il numero di un frame specificato.                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | Recupera gli identificatori di protocollo (e i relativi offset) di tutti i protocolli riconosciuti. |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | Recupera l'offset nell'indirizzo di origine di un frame specificato.                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | Recupera la lunghezza di un frame specificato.                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | Recupera il timestamp di un frame specificato.                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | Recupera l'istanza precedente di un protocollo specificato.                                |
| [GetProperty](getproperty.md)                                         | Recupera una proprietà con un nome specificato.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Recupera le informazioni di una proprietà specifica.                                   |
| [GetPropertyText](getpropertytext.md)                                 | Recupera il testo di una determinata proprietà.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Recupera un protocollo specifico in base al nome.                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | Usa l'handle di protocollo per recuperare i dati relativi al protocollo.                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | Recupera l'offset di un protocollo specificato.                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | Converte un tipo MAC in un tipo di indirizzo.                                             |
| [ModifyFrame](modifyframe.md)                                         | Aggiorna un frame esistente con nuovi dati.                                            |



 

Per ulteriori informazioni sulle funzioni e sulle strutture utilizzate solo da esperti e funzioni e strutture utilizzate solo dai parser, vedere gli argomenti elencati nella tabella seguente.



| Per altre informazioni su                                          | Vedere                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Funzioni specifiche di esperti che è possibile utilizzare per sviluppare dll di esperti. | [Funzioni, strutture ed enumerazioni di esperti](expert-functions-structures-and-enumerations.md) |
| Funzioni specifiche del parser che è possibile usare per sviluppare dll del parser. | [Funzioni e strutture del parser](parser-functions-and-structures.md)                             |



 

 

 



