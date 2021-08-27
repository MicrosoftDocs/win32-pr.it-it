---
title: Oggetto Lettore
description: Oggetto Lettore
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media Format SDK, oggetti reader
- Advanced Systems Format (ASF), oggetti reader
- ASF (Advanced Systems Format), oggetti reader
- oggetti, oggetti reader
- oggetti reader, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1c01b824bbe278991f1512e963a6dde1727c00e73b3c17f5ab4c5556534b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089710"
---
# <a name="reader-object"></a>Oggetto Lettore

L'oggetto reader legge esempi di dati da file multimediali. L'oggetto lettore supporta attualmente i file che usano la struttura di file ASF (Advanced Systems Format) e i file MP3. I dati recapitati dall'oggetto lettore sono non compressi e pronti per il rendering per impostazione predefinita, anche se i campioni possono essere recapitati senza essere decompressi, se necessario. Gli esempi vengono recapitati in modo asincrono dall'oggetto reader. È necessario configurare una funzione di callback per riceverle. Per la riproduzione sincrona dei file ASF, usare l'oggetto lettore sincrono. Né il lettore né il lettore sincrono eseguono il rendering dei dati. È necessario fornire routine di rendering per visualizzare i file multimediali recuperati da un file.

Quando un file contiene supporti codificati che possono essere decodificati con un codec supportato dall'oggetto lettore, è possibile controllare il formato dell'output non compresso. Per modificare il formato dell'output decompresso per un flusso, è necessario recuperare l'oggetto delle proprietà multimediali di output predefinito per tale flusso, apportarvi modifiche e riassegnarlo al flusso nel lettore. Gli oggetti proprietà multimediali di output sono subordinati all'oggetto reader e devono essere creati solo usando il metodo [**IWMReader::GetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops)

L'oggetto reader viene creato dalla funzione [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader), che imposta un puntatore a **un'interfaccia IWMReader.** Le altre interfacce dell'oggetto reader possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto reader.



| Interfaccia                                                    | Descrizione                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | Fornisce l'accesso all'orologio di sistema utilizzato dal lettore.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Gestisce l'acquisizione delle licenze, [*le proprietà DRM*](wmformat-glossary.md) e l'individualizzazione dei client.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Fornisce l'accesso alle licenze che usano i livelli di protezione dell'output (OPL) per specificare i diritti.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Imposta e recupera informazioni sull'intestazione, inclusi metadati, [*marcatori*](wmformat-glossary.md)e dati di script.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Recupera informazioni sui codec usati per codificare il contenuto nel file. Eredita tutti i metodi di **IWMHeaderInfo.**                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Supporta attributi di grandi dimensioni, nomi di attributi duplicati e supporto per più lingue. Eredita tutti i metodi di **IWMHeaderInfo e** **IWMHeaderInfo2.**              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Recupera le dimensioni del pacchetto più grande nel file caricato nel lettore.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Recupera le dimensioni del pacchetto più piccolo nel file caricato nel lettore.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Fornisce l'accesso alle informazioni sul profilo del file caricato nel lettore.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Recupera l'identificatore univoco globale (GUID), se presente, associato al profilo. Eredita tutti i metodi di **IWMProfile.**                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Supporta la condivisione della larghezza di banda e le informazioni di definizione delle priorità del flusso nel profilo. Eredita tutti i metodi di **IWMProfile** e **IWMProfile2.**                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Fornisce funzionalità di base per la lettura di file, incluse operazioni quali apertura, chiusura, avvio, sospensione, ripresa, arresto e recupero e impostazione delle proprietà di output.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Comunica con l'accelerazione video DirectX.                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Fornisce funzionalità avanzate del lettore, ad esempio un orologio fornito dall'utente, l'allocazione del buffer, la restituzione di statistiche e le notifiche di selezione del flusso.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Fornisce un'ulteriore gamma di metodi avanzati per un oggetto lettore esistente. Eredita tutti i metodi di **IWMReaderAdvanced.**                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Fornisce funzionalità avanzate di ricerca e controllo dello streaming. Eredita tutti i metodi di **IWMReaderAdvanced** e **IWMReaderAdvanced2.**                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Fornisce opzioni avanzate per il lettore, incluso il supporto per più lingue. Eredita tutti i metodi di **IWMReaderAdvanced**, **IWMReaderAdvanced2** e **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Controlla le impostazioni di configurazione di rete.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Fornisce l'accesso alle impostazioni di configurazione di rete avanzate. Eredita tutti i metodi di **IWMReaderNetworkConfig.**                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Imposta e annulla i timer sugli orologi del flusso e recupera il valore corrente di un clock di flusso specificato.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Fornisce informazioni sugli intervalli time code SMPTE nel file caricato nel lettore.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Verifica se le modifiche alle proprietà di output di un flusso funzionano correttamente.                                                                                                |



 

Le interfacce di callback seguenti possono essere implementate nell'applicazione per tenere traccia dello stato di avanzamento di un oggetto lettore.



| Interfaccia                                                      | Descrizione                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Acquisisce le credenziali degli utenti e verifica che siano autorizzati ad accedere a un sito remoto.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Fornisce alternative espanse ai **metodi AllocateForOutput** e **AllocateForStream** dell'interfaccia **IWMReaderCallbackAdvanced.** |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Fornisce metodi di callback per **i metodi Start** e **Open** di **IWMReader.**                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Fornisce metodi di callback per i metodi [**dell'interfaccia IWMReaderAdvanced.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Obbligatorio quando le informazioni sullo stato devono essere comunicate all'applicazione host.                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> <dt>

[**Oggetto lettore sincrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




