---
title: Invio di dati ASF a un punto di pubblicazione
description: Invio di dati ASF a un punto di pubblicazione
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK, invio di dati ASF
- Windows Media Format SDK, punti di pubblicazione
- Formato di sistemi avanzati (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
- Formato di sistemi avanzati (ASF), punti di pubblicazione
- ASF (formato avanzato dei sistemi), punti di pubblicazione
- punti di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724125"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Invio di dati ASF a un punto di pubblicazione

È possibile utilizzare Windows Media Format SDK per eseguire il push dei dati ASF a un punto di pubblicazione in un server Windows Media. Il server trasmette quindi i dati dal punto di pubblicazione. Questo scenario è utile se si intende acquisire o ricodificare il contenuto in un computer e si desidera distribuire il contenuto da un altro computer (o più computer). È utile anche se è necessario spostare il contenuto da un computer all'interno di un firewall a un server Windows Media all'esterno del firewall, perché la distribuzione push usa il protocollo HTTP.

> [!Note]  
> Un *punto di pubblicazione* funziona essenzialmente come un redirector. Il client specifica il punto di pubblicazione nell'URL (ad esempio, mms://MyServer/MyPublishingPoint) e il server lo converte in una richiesta di contenuto.

 

Per eseguire il push dei dati nel punto di pubblicazione, alleghi l'oggetto sink push all'oggetto writer. Il sink di push viene utilizzato per aprire la connessione al server e gestire la sessione di push. L'oggetto writer gestisce tutti gli altri aspetti della creazione del file.

Eseguire la procedura seguente:

1.  Creare l'oggetto writer chiamando la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , che restituisce un puntatore [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .
2.  Creare l'oggetto sink di push chiamando la funzione [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , che restituisce un puntatore [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .
3.  Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sul writer, con un puntatore all'interfaccia **IWMWriterPushSink** del sink di rete.
4.  Connettersi al server chiamando [**IWMWriterPushSink:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Scrivere il flusso. Questo passaggio prevede l'impostazione del profilo nell'oggetto writer, l'invio di esempi al writer e possibilmente altre attività. Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md). Altre attività possono includere l'impostazione degli attributi dei metadati (come descritto in [uso dei metadati](working-with-metadata.md)) o l'impostazione di DRM Live nel flusso (come descritto in [Abilitazione del supporto DRM](enabling-drm-support.md)). Queste attività vengono eseguite esattamente come per la scrittura di file ASF.
6.  Al termine della scrittura, chiamare [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sul writer per scollegare l'oggetto sink di push.
7.  Chiamare [**IWMWriterPushSink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) sul sink di push per terminare la sessione con il server.

Questi passaggi sono illustrati nell'applicazione di esempio WMVNetWrite.

> [!Note]  
> Se si invia un file di solo video con velocità in bit molto bassa, è possibile che non si avvii la riproduzione nel punto di pubblicazione per alcuni secondi. Questo problema può verificarsi in diversi casi, ad esempio quando un singolo pacchetto contiene molti piccoli fotogrammi video e nessun audio, oppure quando si verifica un periodo di tempo prolungato tra il primo pacchetto e il secondo pacchetto in un file di solo video a bassa velocità. Per evitare questo problema, inserire un flusso audio invisibile all'utente nel file.

 

## <a name="authentication"></a>Authentication

L'autenticazione al server viene gestita automaticamente dall'oggetto sink di push. Tuttavia, potrebbe essere necessario specificare le credenziali per l'applicazione. Questa operazione viene eseguita tramite l'interfaccia di callback **IWMCredentialCallback** , come indicato di seguito:

1.  Implementare l'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) e [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) nell'applicazione.
2.  Eseguire una query sull'oggetto sink push per l'interfaccia [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .
3.  Chiamare [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) con un puntatore all'interfaccia **IWMStatusCallback** dell'applicazione.
4.  Se il sink di push deve ottenere le credenziali dall'applicazione, esegue una query sul puntatore **IWMStatusCallback** per l'interfaccia **IWMCredentialCallback** e chiama [**IWMCredentialCallback:: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Per informazioni su questo metodo, vedere [Authentication](authentication.md).
5.  Al termine, chiamare [**IWMRegisterCallback:: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) per arrestare il recupero delle notifiche degli eventi dal sink di push.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Invio di dati ASF in una rete**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> <dt>

[**Oggetto sink push writer**](writer-push-sink-object.md)
</dt> </dl>

 

 




