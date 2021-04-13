---
title: Oggetti (Windows Media Format 11 SDK)
description: Oggetti
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows Media Format SDK, oggetti
- ASF (Advanced Systems Format), oggetti
- ASF (formato avanzato dei sistemi), oggetti
- oggetti, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d73672891395d6491009e1c62fac1f9eb81dfe
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400180"
---
# <a name="objects-windows-media-format-11-sdk"></a>Oggetti (Windows Media Format 11 SDK)

Windows Media Format SDK utilizza diversi oggetti per leggere, scrivere, modificare e indicizzare i file ASF e per creare e modificare i profili. Ogni oggetto supporta una serie di interfacce. Alcune interfacce sono supportate in più oggetti. In questi casi, le eventuali differenze nell'implementazione sono illustrate nella sezione di riferimento per l'interfaccia.

Gli oggetti in Windows Media Format SDK sono conformi a COM. Per semplificare lo sviluppo, a ogni oggetto è associato un metodo o una funzione di creazione. È necessario creare oggetti usando la funzione o il metodo di creazione invece di usare manualmente la funzione COM **CoCreateInstance**.

Alcune interfacce hanno un numero aggiunto ai rispettivi nomi, ad esempio **IWMProfile2** e **IWMWriter3**. In ogni caso, le versioni numerate ereditano tutti i metodi delle versioni precedenti e aggiungono una nuova funzionalità.

In ogni pagina oggetto di questo riferimento, le interfacce incluse nell'oggetto COM principale vengono elencate per prime, seguite dalle interfacce di callback che devono essere implementate dall'applicazione.

La tabella seguente elenca gli oggetti supportati da questo SDK con una descrizione della funzionalità di ogni e della funzione usata per crearla.



| Oggetto                                                          | Descrizione                                                                                                                                              | Funzione Creation                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Ripristino di backup](backup-restorer-object.md)                   | Esegue il backup delle licenze, in genere su supporti rimovibili, quindi Ripristina tali licenze in un computer diverso.                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [Registrazione del dispositivo](device-registration-object.md)           | Gestisce il database di registrazione del dispositivo, che contiene le voci per i dispositivi di riproduzione multimediale disponibili tramite una connessione di rete.             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [Transcryptor DRM](drm-transcryptor-object.md)                 | Converte i dati multimediali protetti da DRM in un flusso di dati che può essere inviato ai dispositivi che usano il protocollo Windows Media DRM 10 per i dispositivi di rete. | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [Indicizzatore](indexer-object.md)                                   | Crea un indice per i file ASF per consentire la ricerca nei file con flussi video.                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [Agente di revoca licenze](license-revocation-agent-object.md) | Gestisce la revoca delle licenze.                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [Metadata Editor](metadata-editor-object.md)                   | Modifica i metadati in un'intestazione di file ASF.                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [Gestione profili](profile-manager-object.md)                   | Fornisce interfacce per creare, caricare e salvare i profili. Per scrivere un file ASF, è necessario un profilo.                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [Lettore](reader-object.md)                                     | Legge i file ASF. Questo oggetto utilizza un modello di chiamata asincrono per le relative operazioni.                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [Lettore sincrono](synchronous-reader-object.md)             | Legge i file ASF usando le chiamate sincrone.                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [Writer](writer-object.md)                                     | Scrive i file ASF.                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [Sink di file writer](writer-file-sink-object.md)                 | Controlla i file ASF scritti dall'oggetto writer.                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [Sink di rete writer](writer-network-sink-object.md)           | Controlla lo streaming di rete Live di file ASF scritti dall'oggetto writer.                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [Sink push writer](writer-push-sink-object.md)                 | Controlla il recapito del contenuto di streaming ai server di pubblicazione.                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

Nella tabella seguente sono elencati gli oggetti che dipendono da altri oggetti. Questi oggetti vengono creati da metodi di oggetti esistenti.



| Oggetto                                                        | Descrizione                                                                                                                                                                                                                                                                                                                           | Metodo di creazione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Condivisione della larghezza di banda](bandwidth-sharing-object.md)             | Gestisce le informazioni sulla condivisione della larghezza di banda in un profilo. Per un profilo può esistere più di un oggetto di condivisione della larghezza di banda. Esistono diversi metodi per la creazione di un oggetto di condivisione della larghezza di banda, a seconda che si desideri creare un nuovo oggetto di condivisione della larghezza di banda o accedere a uno esistente.                                           | [**IWMProfile3:: CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) O<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | Contiene un esempio di supporto e tutte le estensioni di unità dati associate. Utilizzato per la scrittura e la lettura di esempi.                                                                                                                                                                                                                           | [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) O<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> OR<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> OR<br/> Creato automaticamente dall'oggetto Reader o dall'oggetto Reader sincrono per il recapito di esempio.<br/> |
| [Proprietà supporto di input](input-media-properties-object.md)   | Gestisce le proprietà di un input. Per ogni input può esistere un oggetto proprietà di input.                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [Esclusione reciproca](mutual-exclusion-object.md)               | Gestisce le informazioni di esclusione reciproca in un profilo. Gli usi comuni per l'esclusione reciproca sono contenuti a più velocità in bit e Soundtrack in diversi linguaggi. Esistono diversi metodi per la creazione di un oggetto di esclusione reciproca a seconda che si desideri creare un nuovo oggetto di esclusione reciproca o accedere a uno esistente.         | [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) O<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [Proprietà supporto di output](output-media-properties-object.md) | Gestisce le proprietà di un output. Per ogni output può esistere un oggetto proprietà del supporto di output. Questi oggetti possono essere creati dal Reader o dal lettore sincrono                                                                                                                                                            | [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) O<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [Profilo](profile-object.md)                                 | Contiene i dati di un profilo durante la modifica. Gli oggetti profilo vengono creati ogni volta che è necessario modificare il profilo. Esistono diversi metodi per creare un oggetto profilo, a seconda che si desideri creare un nuovo profilo o accedere a uno esistente.                                                  | [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) O<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> OR<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> OR<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [Configurazione flusso](stream-configuration-object.md)       | Gestisce le proprietà di un flusso all'interno di un profilo. Gli oggetti di configurazione del flusso vengono creati dagli oggetti flusso ogni volta che è necessario accedere alle informazioni su un flusso. Esistono diversi metodi per la creazione di un oggetto di configurazione del flusso, a seconda che si desideri creare un nuovo flusso o un nuovo accesso o uno esistente. | [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) O<br/> [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> OR<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [Assegnazione di priorità al flusso](stream-prioritization-object.md)     | Mantiene l'elenco di priorità del flusso per un profilo. I flussi verranno rilasciati in ordine di priorità crescente se la larghezza di banda disponibile è limitata. In un profilo può essere presente un solo oggetto di assegnazione di priorità del flusso.                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 





