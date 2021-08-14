---
title: Invio di dati ASF a un punto di pubblicazione
description: Invio di dati ASF a un punto di pubblicazione
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK, invio di dati ASF
- Windows MEDIA Format SDK, punti di pubblicazione
- Advanced Systems Format (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
- Advanced Systems Format (ASF), punti di pubblicazione
- ASF (Advanced Systems Format), punti di pubblicazione
- punti di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f70c1a49ea7ff6272d0eef9f1a51ff79ec216ed9af445c3078d59dd19841dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197540"
---
# <a name="sending-asf-data-to-a-publishing-point"></a>Invio di dati ASF a un punto di pubblicazione

È possibile usare l'SDK Windows Media Format per eseguire il push dei dati ASF in un punto di pubblicazione in un server Windows Media. Il server trasmette quindi i dati da tale punto di pubblicazione. Questo scenario è utile se si acquisisce o si ri-codifica il contenuto in un computer e si vuole distribuire il contenuto da un altro computer (o da più computer). È utile anche se è necessario spostare il contenuto da un computer all'interno di un firewall a un server multimediale Windows all'esterno del firewall, perché la distribuzione push usa il protocollo HTTP.

> [!Note]  
> Un *punto di pubblicazione* agisce essenzialmente come un redirector. Il client specifica il punto di pubblicazione nell'URL (ad esempio, mms://MyServer/MyPublishingPoint) e il server lo converte in una richiesta di contenuto.

 

Per eseguire il push dei dati nel punto di pubblicazione, collegare l'oggetto sink di push all'oggetto writer. Il sink di push viene usato per aprire la connessione al server e gestire la sessione push. L'oggetto writer gestisce tutti gli altri aspetti della creazione del file.

Eseguire la procedura seguente:

1.  Creare l'oggetto writer chiamando la [**funzione WMCreateWriter,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) che restituisce un [**puntatore IWMWriter.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
2.  Creare l'oggetto sink push chiamando la [**funzione WMCreateWriterPushSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) che restituisce un [**puntatore IWMWriterPushSink.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)
3.  Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) nel writer, con un puntatore all'interfaccia **IWMWriterPushSink** del sink di rete.
4.  Connessione al server chiamando [**IWMWriterPushSink::Connessione**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).
5.  Scrivere il flusso. Questo passaggio prevede l'impostazione del profilo nell'oggetto writer, l'invio di esempi al writer e possibilmente altre attività. Per altre informazioni, vedere [Scrittura di file ASF.](writing-asf-files.md) Altre attività possono includere l'impostazione degli attributi dei metadati (come descritto [in](working-with-metadata.md)Uso dei metadati ) o l'impostazione di DRM live nel flusso (come descritto in [Abilitazione del supporto DRM](enabling-drm-support.md)). Queste attività vengono eseguite esattamente come per la scrittura di file ASF.
6.  Al termine della scrittura, chiamare [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) nel writer per scollegare l'oggetto sink push.
7.  Chiamare [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) sul sink push per terminare la sessione con il server.

Questi passaggi sono illustrati nell'applicazione di esempio WMVNetWrite.

> [!Note]  
> Se si invia un file di solo video a velocità in bit molto bassa, la riproduzione potrebbe non iniziare nel punto di pubblicazione per alcuni secondi. Ciò può verificarsi in diversi casi, ad esempio quando un singolo pacchetto contiene molti fotogrammi video di piccole dimensioni e nessun audio o quando si verifica un lungo intervallo di tempo tra il primo e il secondo pacchetto in un file di solo video a bassa velocità in bit. Per evitare questo problema, inserire un flusso audio invisibile all'utente nel file.

 

## <a name="authentication"></a>Autenticazione

L'autenticazione al server viene gestita automaticamente dall'oggetto sink di push. Tuttavia, l'applicazione potrebbe dover fornire le credenziali. Questa operazione viene eseguita tramite l'interfaccia di callback **IWMCredentialCallback,** come indicato di seguito:

1.  Implementare [**l'interfaccia IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) [**e IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) nell'applicazione.
2.  Eseguire una query sull'oggetto sink push per [**l'interfaccia IWMRegisterCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
3.  Chiamare [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) con un puntatore **all'interfaccia IWMStatusCallback** dell'applicazione.
4.  Se il sink push deve ottenere le credenziali dall'applicazione, esegue una query sul puntatore **IWMStatusCallback** per **l'interfaccia IWMCredentialCallback** e chiama [**IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials). Per informazioni su questo metodo, vedere [Autenticazione](authentication.md).
5.  Al termine, chiamare [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) per arrestare il recupero delle notifiche degli eventi dal sink push.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Invio di dati ASF in rete**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> <dt>

[**Oggetto sink push writer**](writer-push-sink-object.md)
</dt> </dl>

 

 




