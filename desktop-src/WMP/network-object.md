---
title: Oggetto di rete
description: L'oggetto di rete fornisce le proprietà e i metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Windows oggetto di rete Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104398076"
---
# <a name="network-object"></a>Oggetto di rete

L'oggetto di **rete** fornisce le proprietà e i metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.

L'oggetto di **rete** supporta le seguenti proprietà.



| Proprietà                                           | Descrizione                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Banda](network-bandwidth.md)                 | Recupera la larghezza di banda corrente dell'elemento multimediale.                                          |
| [Velocità in bit](network-bitrate.md)                     | Recupera la velocità in bit corrente ricevuta.                                              |
| [bufferingCount](network-bufferingcount.md)       | Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione.                           |
| [bufferingProgress](network-bufferingprogress.md) | Recupera la percentuale di memorizzazione nel buffer completata.                                            |
| [bufferingTime](network-bufferingtime.md)         | Specifica o recupera la quantità di tempo di memorizzazione nel buffer in millisecondi prima che inizi la riproduzione. |
| [downloadProgress](network-downloadprogress.md)   | Recupera la percentuale di download completato.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto.                             |
| [frameRate](network-framerate.md)                 | Recupera la frequenza dei fotogrammi video corrente.                                                     |
| [framesSkipped](network-framesskipped.md)         | Recupera il numero totale di frame ignorati durante la riproduzione.                               |
| [lostPackets](network-lostpackets.md)             | Recupera il numero di pacchetti persi.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Specifica o recupera la larghezza di banda massima consentita.                                       |
| [maxBitRate](network-maxbitrate.md)               | Recupera la velocità in bit video massima possibile.                                              |
| [receivedPackets](network-receivedpackets.md)     | Recupera il numero di pacchetti ricevuti.                                                   |
| [receptionQuality](network-receptionquality.md)   | Recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Recupera il numero di pacchetti ripristinati.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Recupera il protocollo di origine utilizzato per ricevere i dati.                                         |



 

L'oggetto di **rete** supporta i metodi seguenti.



| Metodo                                                       | Descrizione                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Recupera un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Recupera l'elenco di eccezioni del proxy.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Recupera il nome di un server proxy da utilizzare.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Recupera la porta del proxy da utilizzare.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Recupera l'impostazione del proxy per un protocollo specificato.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Specifica un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Specifica l'elenco di eccezioni del proxy.                                                                                  |
| [seproxyname](network-setproxyname.md)                     | Specifica il nome di un server proxy da utilizzare.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Specifica la porta del proxy da utilizzare.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Specifica l'impostazione del proxy per un protocollo specificato.                                                                    |



 

È possibile accedere all'oggetto di **rete** tramite la proprietà seguente.



| Oggetto                      | Proprietà                      |
|-----------------------------|-------------------------------|
| [Player](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




