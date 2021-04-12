---
title: Oggetto Lettore
description: Oggetto Lettore
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media Format SDK, oggetti Reader
- ASF (Advanced Systems Format), oggetti Reader
- ASF (formato avanzato dei sistemi), oggetti Reader
- oggetti, oggetti Reader
- oggetti Reader, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398805"
---
# <a name="reader-object"></a>Oggetto Lettore

L'oggetto Reader legge gli esempi di dati dai file multimediali. L'oggetto Reader supporta attualmente i file che usano la struttura di file ASF (Advanced Systems Format) e i file MP3. I dati recapitati dall'oggetto Reader sono decompressi e sono pronti per il rendering per impostazione predefinita, ma gli esempi possono essere recapitati senza essere decompressi se lo si desidera. Gli esempi vengono recapitati in modo asincrono dall'oggetto Reader. è necessario configurare una funzione di callback per riceverli. Per la riproduzione sincrona dei file ASF, utilizzare l'oggetto Reader sincrono. Né il Reader né il lettore sincrono eseguono il rendering dei dati. È necessario fornire routine di rendering personalizzate per visualizzare il supporto recuperato da un file.

Quando un file contiene un supporto codificato che può essere decodificato con un codec supportato dall'oggetto Reader, è possibile controllare il formato dell'output non compresso. Per modificare il formato dell'output decompresso per un flusso, è necessario recuperare l'oggetto proprietà del supporto di output predefinito per il flusso, apportare le modifiche e riassegnarlo al flusso del lettore. Gli oggetti proprietà del supporto di output sono subordinati all'oggetto Reader e devono essere creati solo usando il metodo [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) .

L'oggetto Reader viene creato dalla funzione [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader), che imposta un puntatore a un'interfaccia **IWMReader** . Le altre interfacce dell'oggetto Reader possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto Reader.



| Interfaccia                                                    | Descrizione                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Consente di accedere al clock di sistema utilizzato dal reader.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Gestisce l'acquisizione delle licenze, le proprietà [*DRM*](wmformat-glossary.md) e l'individualizzazione del client.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Consente di accedere alle licenze che usano i livelli di protezione dell'output (OPL) per specificare i diritti.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Imposta e recupera le informazioni di intestazione, inclusi i metadati, i [*marcatori*](wmformat-glossary.md)e i dati di script.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Recupera le informazioni sui codec utilizzati per codificare il contenuto del file. Eredita tutti i metodi di **IWMHeaderInfo**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Supporta le dimensioni degli attributi grandi, i nomi di attributi duplicati e il supporto di più lingue. Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Recupera la dimensione del pacchetto più grande nel file caricato nel lettore.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Recupera le dimensioni del pacchetto più piccolo nel file caricato nel lettore.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Consente di accedere alle informazioni sul profilo del file caricato nel lettore.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Recupera l'identificatore univoco globale (GUID), se presente, associato al profilo. Eredita tutti i metodi di **IWMProfile**.                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Supporta la condivisione della larghezza di banda e le informazioni relative alla priorità del flusso nel profilo. Eredita tutti i metodi di **IWMProfile** e **IWMProfile2**.                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Fornisce le funzionalità di base per la lettura dei file, incluse operazioni quali apertura, chiusura, avvio, sospensione, ripresa, arresto e recupero e impostazione delle proprietà di output.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Comunica con l'accelerazione video DirectX.                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Fornisce funzionalità avanzate del lettore, ad esempio un orologio fornito dall'utente, l'allocazione del buffer, le statistiche di ritorno e le notifiche di selezione dei flussi.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Fornisce un intervallo aggiuntivo di metodi avanzati per un oggetto Reader esistente. Eredita tutti i metodi di **IWMReaderAdvanced**.                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Fornisce il controllo di flusso e ricerca avanzata. Eredita tutti i metodi di **IWMReaderAdvanced** e **IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Fornisce opzioni avanzate per il lettore, incluso il supporto per più lingue. Eredita tutti i metodi di **IWMReaderAdvanced**, **IWMReaderAdvanced2** e **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Controlla le impostazioni di configurazione di rete.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Consente di accedere alle impostazioni di configurazione di rete avanzate. Eredita tutti i metodi di **IWMReaderNetworkConfig**.                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Imposta e Annulla i timer sugli orologi del flusso e recupera il valore corrente di un clock del flusso specificato.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Fornisce informazioni sugli intervalli di codice di ora SMPTE nel file caricato nel lettore.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Verifica se le modifiche apportate alle proprietà di output di un flusso funzionano correttamente.                                                                                                |



 

Le interfacce di callback seguenti possono essere implementate nell'applicazione per tenere traccia dello stato di avanzamento di un oggetto Reader.



| Interfaccia                                                      | Descrizione                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Acquisisce le credenziali degli utenti e verifica che dispongano delle autorizzazioni per accedere a un sito remoto.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Fornisce alternative estese ai metodi **AllocateForOutput** e **AllocateForStream** dell'interfaccia **IWMReaderCallbackAdvanced** . |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Fornisce metodi di callback per i metodi di **avvio** e **apertura** di **IWMReader**.                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Fornisce metodi di callback per i metodi dell'interfaccia [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) .                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host.                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




