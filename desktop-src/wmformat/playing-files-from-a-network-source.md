---
title: Riproduzione di file da un'origine di rete
description: Riproduzione di file da un'origine di rete
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows Media Format SDK, lettura di dati ASF
- Windows Media Format SDK, riproduzione di file da origini di rete
- Formato di sistemi avanzati (ASF), lettura dati
- ASF (Advanced Systems Format), lettura di dati
- ASF (Advanced Systems Format), riproduzione di file da origini di rete
- ASF (Advanced Systems Format), riproduzione di file da origini di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1e4e41ddf94498ddeddf90e64439c1b11b7ba8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299528"
---
# <a name="playing-files-from-a-network-source"></a>Riproduzione di file da un'origine di rete

La lettura da una rete non è sostanzialmente diversa dalla lettura di un file locale. L'applicazione passa l'URL al metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) dell'oggetto Reader e l'oggetto Reader gestisce i dettagli dei protocolli di rete. L'oggetto Reader utilizza la gestione intelligente del buffer per garantire la riproduzione più semplice possibile. Se l'applicazione necessita di un maggiore controllo sulle impostazioni di rete dell'oggetto Reader, queste sono disponibili tramite le interfacce [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) e [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) .

Il contenuto di un'origine di rete rientra in una delle due categorie seguenti:

-   Streaming. I dati vengono trasmessi solo nel tempo per essere riprodotti nel computer locale. I server che eseguono servizi Windows Media possono fornire dati di streaming. Se viene eseguito il flusso del contenuto a più velocità in bit (MBR), il client può richiedere una velocità in bit diversa dal server durante l'avanzamento del flusso.
-   Scaricato. Tutti i dati vengono trasmessi il più rapidamente possibile in modo che possano essere salvati come file nel computer locale. I server Web forniscono i dati scaricati. Non esiste alcuna comunicazione dal client al server dopo l'inizio del download.

Quando l'oggetto Reader Scarica un file da un server Web, viene usata una tecnica denominata streaming progressivo, che consente a un giocatore di iniziare a eseguire il rendering del contenuto prima del completamento del download. I dati vengono memorizzati nel buffer per fornire un flusso di dati ininterrotti al lettore. Informazioni quali la velocità di trasferimento e la durata del contenuto vengono utilizzate per determinare la durata del buffering dei dati prima di assegnarla al lettore.

Per aprire un file o un flusso in una rete, chiamare il metodo **IWMReader:: Open** dell'oggetto Reader con l'URL appropriato. **Open** è una chiamata asincrona, quindi viene restituito immediatamente. Quando l'origine è pronta per la lettura, l'oggetto Reader invia una \_ notifica WMT aperta al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback dell'applicazione. A questo punto, l'applicazione può eseguire una query sul Reader per la modalità di recapito chiamando [**IWMReaderAdvanced2:: GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Per il contenuto di rete, questo metodo restituirà il \_ download della modalità di riproduzione WMT \_ \_ , indicando il contenuto scaricato o lo \_ streaming in modalità di riproduzione WMT \_ \_ , che indica il contenuto trasmesso.

Per iniziare a leggere il file o il flusso, chiamare il metodo [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) . Il lettore invia una \_ \_ notifica di avvio del buffer WMT quando inizia a memorizzare nel buffer il contenuto e una \_ notifica di arresto del buffer WMT quando il \_ buffering è completo. Mentre il lettore memorizza nel buffer il contenuto, ovvero tra queste due notifiche, potrebbe essere necessario visualizzare l'avanzamento del buffering all'utente. Il metodo [**IWMReaderAdvanced2:: GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) restituisce la percentuale di dati memorizzati nel buffer e il tempo stimato rimanente. Per il contenuto scaricato, è anche possibile chiamare [**IWMReaderAdvanced2:: GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) per ottenere lo stato del download. Chiamare questi metodi ripetutamente per aggiornare la visualizzazione, fino a quando il buffering non viene completato. Il buffering può verificarsi di nuovo durante la riproduzione, a causa di fattori quali la congestione della rete. In tal caso, l'applicazione riceve un'altra \_ notifica di avvio del buffer WMT \_ .

Quando l'oggetto Reader inizia a riprodurre il contenuto, invia una \_ notifica avviata da WMT. Poiché ogni campione viene decodificato e diventa disponibile per il rendering, il lettore lo passa all'applicazione tramite il metodo di callback [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) . A questo punto, il processo è identico a quello per la riproduzione di file locali. Quando la riproduzione viene arrestata, il lettore invia una \_ \_ notifica di WMT end of \_ streaming.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




