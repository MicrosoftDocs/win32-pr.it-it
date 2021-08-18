---
title: Oggetto di rete
description: L'oggetto Network fornisce proprietà e metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Oggetti di rete Windows Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bf91c23d6a5c581430b17a370e66027a5f9174d0511a2647fba33834ec6c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996111"
---
# <a name="network-object"></a>Oggetto di rete

**L'oggetto Network** fornisce proprietà e metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.

**L'oggetto** Network supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Banda](network-bandwidth.md)                 | Recupera la larghezza di banda corrente dell'elemento multimediale.                                          |
| [Bitrate](network-bitrate.md)                     | Recupera la velocità in bit corrente ricevuta.                                              |
| [bufferingCount](network-bufferingcount.md)       | Recupera il numero di volte in cui si è verificata la memorizzazione nel buffer durante la riproduzione.                           |
| [bufferingProgress](network-bufferingprogress.md) | Recupera la percentuale di memorizzazione nel buffer completata.                                            |
| [bufferingTime](network-bufferingtime.md)         | Specifica o recupera la quantità di tempo di memorizzazione nel buffer in millisecondi prima dell'inizio della riproduzione. |
| [downloadProgress](network-downloadprogress.md)   | Recupera la percentuale di download completata.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto.                             |
| [Framerate](network-framerate.md)                 | Recupera la frequenza fotogrammi video corrente.                                                     |
| [framesSkipped](network-framesskipped.md)         | Recupera il numero totale di fotogrammi ignorati durante la riproduzione.                               |
| [lostPackets](network-lostpackets.md)             | Recupera il numero di pacchetti persi.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Specifica o recupera la larghezza di banda massima consentita.                                       |
| [maxBitRate](network-maxbitrate.md)               | Recupera la velocità in bit video massima possibile.                                              |
| [receivedPackets](network-receivedpackets.md)     | Recupera il numero di pacchetti ricevuti.                                                   |
| [receptionQuality](network-receptionquality.md)   | Recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Recupera il numero di pacchetti recuperati.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Recupera il protocollo di origine utilizzato per ricevere i dati.                                         |



 

**L'oggetto** Network supporta i metodi seguenti.



| Metodo                                                       | Descrizione                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Recupera un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Recupera l'elenco di eccezioni proxy.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Recupera il nome di un server proxy da utilizzare.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Recupera la porta proxy da utilizzare.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Recupera l'impostazione proxy per un protocollo specificato.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Specifica un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Specifica l'elenco di eccezioni proxy.                                                                                  |
| [setProxyName](network-setproxyname.md)                     | Specifica il nome di un server proxy da utilizzare.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Specifica la porta proxy da utilizzare.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Specifica l'impostazione proxy per un protocollo specificato.                                                                    |



 

**L'accesso** all'oggetto Network viene eseguito tramite la proprietà seguente.



| Oggetto                      | Proprietà                      |
|-----------------------------|-------------------------------|
| [Player](player-object.md) | [Rete](player-network.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




