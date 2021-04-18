---
title: Interfaccia IWMPNetwork (VB e C) (WMP. h)
description: Fornisce proprietà e metodi per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete. L'interfaccia IWMPNetwork espone le proprietà seguenti.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Interfaccia IWMPNetwork (VB e C) Windows Media Player
- Interfaccia IWMPNetwork (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327873"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Interfaccia IWMPNetwork (VB e C#)

Fornisce proprietà e metodi per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.

L'interfaccia **IWMPNetwork** espone le proprietà seguenti.

## <a name="members"></a>Membri

L'interfaccia **IWMPNetwork (VB e C#)** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IWMPNetwork (VB e C#)** presenta questi metodi.



| Metodo                                                                                           | Descrizione                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Restituisce un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Restituisce l'elenco di eccezioni del proxy.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Restituisce il nome del server proxy in uso.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Restituisce la porta proxy utilizzata.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Restituisce informazioni sulle impostazioni proxy per un protocollo.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Specifica se il server proxy viene ignorato se il server di origine si trova in una rete locale.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Specifica l'elenco di eccezioni del proxy.<br/>                                                                         |
| [**seproxyname**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Specifica il nome del server proxy da utilizzare.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Specifica la porta del proxy da utilizzare.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Specifica le impostazioni proxy per un protocollo.<br/>                                                                |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IWMPNetwork (VB e C#)** presenta queste proprietà.



| Proprietà                                                                                          | Tipo di accesso           | Descrizione                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Banda**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Sola lettura<br/>  | Ottiene la larghezza di banda corrente dell'elemento multimediale.<br/>                                     |
| [**Velocità in bit**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Sola lettura<br/>  | Ottiene la velocità in bit corrente ricevuta.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Sola lettura<br/>  | Ottiene il numero di volte in cui si è verificato il buffer durante la riproduzione.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Sola lettura<br/>  | Ottiene la percentuale di completamento del buffer.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lettura/Scrittura<br/> | Ottiene o imposta la quantità di tempo di memorizzazione nel buffer in millisecondi prima che inizi la riproduzione.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Sola lettura<br/>  | Ottiene la percentuale di completamento del download.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Sola lettura<br/>  | Ottiene la frequenza dei fotogrammi video specificata dall'autore del contenuto.<br/>                        |
| [**frameRate**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Sola lettura<br/>  | Ottiene la frequenza dei fotogrammi video corrente.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Sola lettura<br/>  | Ottiene il numero totale di frame ignorati durante la riproduzione.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Sola lettura<br/>  | Ottiene il numero di pacchetti persi.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lettura/Scrittura<br/> | Ottiene o imposta la larghezza di banda massima consentita.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Sola lettura<br/>  | Ottiene la velocità in bit video massima possibile.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Sola lettura<br/>  | Ottiene il numero di pacchetti ricevuti.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Sola lettura<br/>  | Ottiene la percentuale di pacchetti non persi negli ultimi 30 secondi.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Sola lettura<br/>  | Ottiene il numero di pacchetti ripristinati.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Sola lettura<br/>  | Ottiene il protocollo di origine utilizzato per ricevere i dati.<br/>                                    |



 

Ottenere un'interfaccia **IWMPNetwork** usando la proprietà seguente.



| Oggetto                                                                   | Proprietà                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**network**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





