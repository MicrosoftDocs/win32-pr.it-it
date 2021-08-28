---
title: Riproduzione di file da un'origine di rete
description: Riproduzione di file da un'origine di rete
ms.assetid: 72f2d685-56fc-4da2-8372-3774cc65f59d
keywords:
- Windows Media Format SDK, lettura dei dati ASF
- Windows Media Format SDK, riproduzione di file da origini di rete
- Advanced Systems Format (ASF), lettura dei dati
- ASF (Advanced Systems Format), lettura dei dati
- Advanced Systems Format (ASF), riproduzione di file da origini di rete
- ASF (Advanced Systems Format), riproduzione di file da origini di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8473a2feb4edd567c15d640dfd20e65c2893fe12de6c25a957cc5f730fde0baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027379"
---
# <a name="playing-files-from-a-network-source"></a>Riproduzione di file da un'origine di rete

La lettura da una rete non è fondamentalmente diversa dalla lettura di un file locale. L'applicazione passa l'URL al metodo [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) dell'oggetto reader e l'oggetto lettore gestisce i dettagli dei protocolli di rete. L'oggetto lettore usa la gestione intelligente del buffer per offrire la riproduzione più uniforme possibile. Se l'applicazione necessita di un maggiore controllo sulle impostazioni di rete dell'oggetto lettore, queste sono disponibili tramite le interfacce [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig) e [**IWMReaderNetworkConfig2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)

Il contenuto di un'origine di rete rientra in una delle due categorie seguenti:

-   Streaming. I dati vengono trasmessi appena in tempo per essere riprodotti nel computer locale. I server che eseguono Servizi Windows Media possono fornire dati di streaming. Se viene trasmesso il contenuto MBR (Multiple Bit Rate), il client può richiedere una velocità in bit diversa dal server con l'avanzamento del flusso.
-   Scaricato. Tutti i dati vengono trasmessi il più rapidamente possibile in modo che possano essere salvati come file nel computer locale. I server Web forniscono i dati scaricati. Dopo l'avvio del download non viene più avviata alcuna comunicazione dal client al server.

Quando l'oggetto lettore scarica un file da un server Web, usa una tecnica denominata streaming progressivo, che consente a un lettore di iniziare a eseguire il rendering del contenuto prima del completamento del download. I dati vengono memorizzati nel buffer per fornire un flusso ininterrompato di dati al lettore. Informazioni come la velocità di trasferimento e la durata del contenuto vengono usate per determinare per quanto tempo bufferare i dati prima di darlo al lettore.

Per aprire un file o un flusso in rete, chiamare il metodo **IWMReader::Open dell'oggetto** lettore con l'URL appropriato. **Open** è una chiamata asincrona, quindi restituisce immediatamente . Quando l'origine è pronta per la lettura, l'oggetto lettore invia una notifica WMT OPENED al metodo \_ di callback [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) dell'applicazione. A questo punto, l'applicazione può eseguire una query sul lettore per la modalità di recapito chiamando [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode). Per il contenuto di rete, questo metodo restituirà WMT PLAY MODE DOWNLOAD, che indica il contenuto scaricato, o \_ \_ \_ WMT PLAY MODE \_ \_ STREAMING, che indica il contenuto \_ trasmesso in streaming.

Per iniziare a leggere il file o il flusso, chiamare il [**metodo IWMReader::Start.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) Il lettore invia una notifica WMT BUFFERING START all'avvio del buffer del contenuto e una notifica WMT BUFFERING STOP al termine \_ \_ della \_ \_ memorizzazione nel buffer. Mentre il lettore sta memorizzazione nel buffer del contenuto, ovvero tra queste due notifiche, potrebbe essere necessario visualizzare lo stato di avanzamento del buffering per l'utente. Il [**metodo IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress) restituisce la percentuale di dati memorizzati nel buffer e il tempo stimato che rimane. Per il contenuto scaricato, è anche possibile chiamare [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress) per ottenere lo stato di avanzamento del download. Chiamare questi metodi ripetutamente per aggiornare la visualizzazione, fino al completamento della memorizzazione nel buffer. La memorizzazione nel buffer può verificarsi nuovamente durante la riproduzione, a causa di fattori quali la congestione della rete. In questo caso, l'applicazione riceve un'altra notifica WMT \_ BUFFERING \_ START.

Quando l'oggetto lettore inizia a riprodurre il contenuto, invia una notifica WMT \_ STARTED. Quando ogni esempio viene decodificato e diventa disponibile per il rendering, il lettore lo passa all'applicazione tramite il metodo di callback [**IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) A questo punto, il processo è identico a quello per la riproduzione di file locali. Quando la riproduzione si arresta, il lettore invia una notifica WMT \_ END \_ OF \_ STREAMING.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




