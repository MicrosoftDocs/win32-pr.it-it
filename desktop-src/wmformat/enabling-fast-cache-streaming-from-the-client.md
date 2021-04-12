---
title: Abilitazione del flusso fast cache dal client
description: Abilitazione del flusso fast cache dal client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK, abilitazione del flusso fast cache
- Windows Media Format SDK, fast cache streaming
- Advanced Systems Format (ASF), abilitazione del flusso fast cache
- ASF (Advanced Systems Format), abilitazione del flusso fast cache
- Advanced Systems Format (ASF), streaming fast cache
- ASF (formato avanzato dei sistemi), streaming fast cache
- flussi, abilitazione del flusso fast cache
- Streaming fast cache, abilitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398569"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Abilitazione del flusso fast cache dal client

Fast cache è una tecnologia di streaming in cui il server opportunisticamente trasmette contenuto a una velocità in bit superiore rispetto a quella necessaria per la riproduzione.

Se la larghezza di banda disponibile è superiore alla velocità in bit del contenuto, i flussi della cache veloce hanno una velocità superiore e il contenuto viene memorizzato nel buffer. Questo consente di ridurre le interruzioni in un secondo momento se la rete viene congestionata. Se la larghezza di banda di rete è inferiore alla velocità in bit del contenuto, la cache veloce memorizza nel buffer una parte dei dati prima che venga avviata la riproduzione. La cache veloce è consigliata per le reti non affidabili, ad esempio reti wireless o reti che riscontrano fluttuazioni di grandi dimensioni nel traffico di rete, ad esempio modem via cavo. È inoltre consigliato per il contenuto della velocità in bit variabile (VBR). I requisiti di larghezza di banda per il contenuto VBR non sono costanti e la cache veloce consente al lettore di memorizzare nel buffer il flusso durante le porzioni a bassa velocità in bit.

Il flusso fast cache è supportato solo per contenuti su richiesta. Inoltre, il server deve essere configurato in modo da usare lo streaming veloce della cache.

Per abilitare la cache veloce nell'oggetto Reader, chiamare i metodi [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) e [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) con il valore **true**. Il primo metodo consente al Reader di memorizzare nella cache il contenuto trasmesso. Il secondo consente di usare la cache veloce in particolare.

Con queste impostazioni, il lettore attiverà fast cache per impostazione predefinita se la larghezza di banda di rete è significativamente superiore o inferiore alla velocità in bit del contenuto e se il server lo supporta. L'utente può inoltre controllare se l'oggetto Reader utilizza la cache veloce aggiungendo uno o più dei modificatori seguenti all'URL.



| Modificatore         | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Se questo modificatore è presente, il valore ' 0' Disabilita in modo esplicito la cache veloce, mentre il valore ' 1' lo Abilita in modo esplicito.                                                                                                                                                                                                                            |
| WMBitrate        | Questo modificatore specifica la velocità in bit massima del server. Questo modificatore può essere usato per limitare la cache veloce a un determinato limite di larghezza di banda. Questo modificatore viene ignorato se una larghezza di banda di connessione esplicita è già impostata con una chiamata a [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth). |
| WMContentBitrate | Questo modificatore specifica la velocità in bit per il contenuto. Il lettore utilizza questo modificatore, se presente, quando seleziona i flussi da un file con velocità in bit multipla (MBR). In questo modo, il lettore può ricevere contenuto a bitrate elevato su una connessione lenta, con tempi e ritardi di buffer molto lunghi.                                          |



 

Il modificatore WMCache = 1 impone al lettore di usare lo streaming veloce della cache, indipendentemente dalla larghezza di banda di rete o dalla velocità in bit del contenuto e indipendentemente dalle chiamate precedenti a **SetEnableFastCache**. Tuttavia, non esegue l'override dell'impostazione **SetEnableContentCaching** nel lettore; né sostituisce la configurazione del server.

I modificatori di URL hanno il formato seguente:

*URL*? *modificatore* = *valore* di

Ad esempio:

mms://MyServer/MyVideo.wmv? WMCache = 1

È possibile specificare più di un modificatore; usare una e commerciale (&) per separarli:

mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000

 

 




