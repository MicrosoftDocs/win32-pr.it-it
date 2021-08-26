---
title: File di libreria e compilatori Impostazioni
description: File di libreria e compilatori Impostazioni
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows MEDIA Format SDK, file di libreria
- Windows Media Format SDK, impostazioni del compilatore
- Windows MEDIA Format SDK, file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176f6c7acb9516e8c7ac38a067091bcbb0c8f7cf49cfdb9e65b396768158b233
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930661"
---
# <a name="library-files-and-compiler-settings"></a>File di libreria e compilatori Impostazioni

Per sviluppare un'applicazione usando Windows Media Format SDK, è necessario usare Microsoft Visual C++ versione 6.0 o successiva. Gli unici linguaggi di programmazione appropriati per lo sviluppo sono C++ e C.

Il contenuto dei vari file di intestazione inclusi in questo SDK è descritto nella tabella seguente.



| File di intestazione                 | Descrizione                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr.h                    | Definisce i codici di errore relativi alle operazioni sui file ASF. Questa intestazione è inclusa in wmsdk.h.                                                                                                                                                            |
| drmexternals.h              | Definisce strutture, enumerazioni e costanti usate per DRM (Digital Rights Management). Includere questa intestazione quando si scrive un'applicazione che usa DRM.                                                                                            |
| dshowasf.h                  | Definisce i filtri QASF DirectShow Microsoft. Includere questa intestazione quando si scrive un'DirectShow che crea o legge i file ASF. Per altre informazioni, vedere DirectShow [e Windows Media](directshow-and-windows-media.md).               |
| msnetobj.h                  | Definisce [**l'interfaccia IRMGetLicense,**](irmgetlicense.md) implementata in una delle librerie di runtime installate con Windows Media Format SDK.                                                                                     |
| nserror.h                   | Definisce i codici di errore per Windows Media Technologies. Solo un subset di questi codici di errore è rilevante per l'SDK Windows Media Format. Questa intestazione è inclusa in wmsdk.h.                                                                            |
| wmdxva.h                    | Include altre intestazioni e definizioni necessarie per abilitare l'accelerazione video Microsoft DirectX per la riproduzione Windows contenuto basato su Media. Per altre informazioni, vedere [Abilitazione dell'accelerazione video DirectX.](enabling-directx-video-acceleration.md) |
| wmnetsourcecreator.h        | Contiene le informazioni necessarie per creare plug-in di origine di rete.                                                                                                                                                                                      |
| wmsbuffer.h                 | Definisce le interfacce utilizzate dagli oggetti buffer. Includere questa intestazione quando si creano buffer personalizzati per la lettura dei file.                                                                                                                                 |
| wmsdk.h                     | Intestazione principale per le applicazioni che usano Windows Media Format SDK. Questa intestazione non contiene definizioni, ma include asferr.h, nserror.h, windows.h e wmsdkidl.h. Includere questa intestazione per tutte le applicazioni che usano questo SDK.                     |
| wmsdkidl.h                  | Definisce le interfacce, le funzioni, le strutture, le enumerazioni e le costanti per la maggior parte degli oggetti di Windows Media Format SDK. Questa intestazione è inclusa in wmsdk.h.                                                                             |
| wmsinternaladminnetsource.h | Definisce le interfacce dei plug-in di origine di rete.                                                                                                                                                                                                  |
| wmsysprf.h                  | Definisce le costanti per i profili di sistema. Includere questa intestazione nelle applicazioni che caricano i profili di sistema in base all'identificatore.                                                                                                                         |



 

Per usare l'SDK Windows Media Format, il compilatore deve essere configurato correttamente. La configurazione è diversa per la compilazione in modalità di debug rispetto alla modalità di rilascio. Configurare l'impostazione in base alla tabella seguente. Tutte queste impostazioni vengono configurate nella Project Impostazioni di dialogo. Per visualizzare la finestra di dialogo, selezionare **Impostazioni** dal menu **Project** comando.



| Impostazione                                                                 | Valore di debug                                                                              | Valore di versione                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (scheda C/C++, Categoria = Generazione del codice) Usare la libreria di runtime            | Eseguire il debug di DLL multithreading                                                                  | DLL multithreading                                                                       |
| (scheda Collegamento, Categoria = Generale) Ignora tutte le librerie predefinite (casella di controllo) | Selezionato                                                                                 | Selezionato                                                                                |
| (scheda Collegamento, Categoria = Generale) Moduli di oggetti/librerie                   | Includere Msvcrtd.lib e Wmvcore.lib.Do non includere Libc.lib o qualsiasi variazione.<br/> | Includere Msvcrt.lib e Wmvcore.lib.Do non includono Libc.lib o alcuna variazione.<br/> |



 

Se si usa Microsoft Visual Studio .NET, le impostazioni sono state modificate in posizioni diverse, come illustrato nella tabella seguente. Tutte queste impostazioni vengono configurate nella **finestra di dialogo Pagine delle** proprietà. Per visualizzare la finestra di dialogo, fare  clic con il pulsante destro del mouse sul progetto nel riquadro Esplora soluzioni e scegliere **Proprietà** dal menu di scelta rapida.



| Impostazione                                                                  | Valore di debug                                                                              | Valore di versione                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Proprietà di configurazione/C/C++ /Generazione di codice) Libreria di runtime     | DLL di debug multi-thread (/MTd)                                                          | DLL multi-thread (/MD)                                                                |
| (Proprietà di configurazione/Linker/Input) Dipendenze aggiuntive      | Includere Msvcrtd.lib e Wmvcore.lib.Do non includere Libc.lib o qualsiasi variazione.<br/> | Includere Msvcrt.lib e Wmvcore.lib.Do non includono Libc.lib o alcuna variazione.<br/> |
| (Proprietà di configurazione/Linker/Input) Ignora tutte le librerie predefinite | Sì                                                                                      | Sì                                                                                     |



 

Se si vuole ritardare il caricamento di Wmvcore.dll o qualsiasi altra DLL, usare l'opzione di collegamento /DELAYLOAD in Microsoft Visual C++ 6.0 o DLL con caricamento ritardato in Microsoft Visual C++ .NET.

È inoltre necessario includere le directory per le librerie e le intestazioni di Windows Media Format SDK. Per trovare le impostazioni della directory Visual C++ 6.0, scegliere Opzioni dal **menu** Strumenti **e** quindi fare clic **sulla scheda** Directory. Quando si Visual C++ .NET,  scegliere Opzioni dal **menu** Strumenti e quindi selezionare Progetti/VC++ directory nell'elenco delle opzioni. Aggiungere directory come illustrato nella tabella seguente. Se è stata modificata la directory di installazione per Windows Media Format SDK, il percorso sarà diverso.



| Tipo di directory | Percorso predefinito                 |
|----------------|------------------------------|
| File di inclusione  | C: \\ WMSDK \\ WMFSDK11 \\ include |
| File di libreria  | C: \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Se si usa Platform SDK, i percorsi predefiniti verranno visualizzati come segue:



| Tipo di directory | Percorso predefinito                                              |
|----------------|-----------------------------------------------------------|
| File di inclusione  | C: \\ Programmi \\ Microsoft SDsK \\ Windows \\ v6.0 \\ Include |
| File di libreria  | C: \\ Programmi \\ Microsoft SDsK \\ Windows \\ v6.0 \\ Lib     |



 

Prima di chiamare una delle funzioni di creazione, COM deve essere inizializzato con una chiamata a **Coinitialize** o **CoinitializeEx**. È possibile usare il modello di threading free o il modello di threading apartment, ma il modello di threading apartment impone restrizioni di threading all'applicazione. Per altre informazioni su Microsoft Component Object Model (COM), vedere la pagina COM nel [sito Web Microsoft](../com/the-component-object-model.md).

**Nota:** Le applicazioni che riproducino o creano file protetti da Digital Rights Management (DRM) richiedono una libreria statica individualizzata che deve essere ottenuta separatamente da Microsoft. Per altre informazioni, vedere il modulo Windows Media Licensing Form nel [sito Web Microsoft](https://www.microsoft.com/licensing/default). Se si usa la libreria DRM, non è necessario collegarsi a Wmvcore.lib.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](getting-started.md)
</dt> </dl>

 

