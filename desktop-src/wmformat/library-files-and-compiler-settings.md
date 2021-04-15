---
title: File di libreria e impostazioni del compilatore
description: File di libreria e impostazioni del compilatore
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows Media Format SDK, file di libreria
- Windows Media Format SDK, impostazioni del compilatore
- Windows Media Format SDK, file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079636c8f01decdcfb90e36641e26c62354a7893
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474561"
---
# <a name="library-files-and-compiler-settings"></a>File di libreria e impostazioni del compilatore

Per sviluppare un'applicazione usando Windows Media Format SDK, è necessario usare Microsoft Visual C++ versione 6,0 o successiva. Gli unici linguaggi di programmazione appropriati per lo sviluppo sono C++ e C.

I contenuti dei vari file di intestazione inclusi in questo SDK sono descritti nella tabella seguente.



| File di intestazione                 | Descrizione                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr. h                    | Definisce i codici di errore relativi alle operazioni sui file ASF. Questa intestazione è inclusa in WMSDK. h.                                                                                                                                                            |
| drmexternals. h              | Definisce le strutture, le enumerazioni e le costanti utilizzate per la Digital Rights Management (DRM). Includere questa intestazione quando si scrive un'applicazione che utilizza DRM.                                                                                            |
| dshowasf. h                  | Definisce i filtri Microsoft DirectShow QASF. Includere questa intestazione quando si scrive un'applicazione DirectShow per la creazione o la lettura di file ASF. Per ulteriori informazioni, vedere [DirectShow e Windows Media](directshow-and-windows-media.md).               |
| msnetobj. h                  | Definisce l'interfaccia [**IRMGetLicense**](irmgetlicense.md) , implementata in una delle librerie di Runtime installate con Windows Media Format SDK.                                                                                     |
| nserror. h                   | Definisce i codici di errore per le tecnologie Windows Media. Solo un subset di questi codici di errore è pertinente per Windows Media Format SDK. Questa intestazione è inclusa in WMSDK. h.                                                                            |
| wmdxva. h                    | Include altre intestazioni e definizioni necessarie per abilitare l'accelerazione video Microsoft DirectX per la riproduzione di contenuto basato su Windows Media. Per altre informazioni, vedere [Abilitazione dell'accelerazione video DirectX](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Contiene le informazioni necessarie per creare plug-in di origine di rete.                                                                                                                                                                                      |
| wmsbuffer. h                 | Definisce le interfacce utilizzate dagli oggetti buffer. Includere questa intestazione quando si creano buffer personalizzati per la lettura dei file.                                                                                                                                 |
| WMSDK. h                     | Intestazione principale per le applicazioni che usano Windows Media Format SDK. Questa intestazione non contiene definizioni, ma include asferr. h, nserror. h, Windows. h e wmsdkidl. h. Includere questa intestazione per tutte le applicazioni che usano questo SDK.                     |
| wmsdkidl. h                  | Definisce le interfacce, le funzioni, le strutture, le enumerazioni e le costanti per la maggior parte degli oggetti di Windows Media Format SDK. Questa intestazione è inclusa in WMSDK. h.                                                                             |
| wmsinternaladminnetsource. h | Definisce le interfacce dei plug-in di origine di rete.                                                                                                                                                                                                  |
| wmsysprf. h                  | Definisce le costanti per i profili di sistema. Includere questa intestazione nelle applicazioni che caricano i profili di sistema in base all'identificatore.                                                                                                                         |



 

Per usare Windows Media Format SDK, il compilatore deve essere configurato correttamente. La configurazione è diversa per la compilazione in modalità di debug rispetto alla modalità di rilascio. Configurare l'impostazione in base alla tabella seguente. Tutte queste impostazioni sono configurate nella finestra di dialogo Impostazioni progetto. Per ottenere la finestra di dialogo, selezionare **Impostazioni** dal menu **progetto** .



| Impostazione                                                                 | Valore di debug                                                                              | Valore versione                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Scheda C/C++, categoria = generazione codice) Utilizzare la libreria di runtime            | Debug DLL multithread                                                                  | DLL multithread                                                                       |
| (Scheda collegamento, categoria = generale) Ignora tutte le librerie predefinite (casella di controllo) | Selezionato                                                                                 | Selezionato                                                                                |
| (Scheda collegamento, categoria = generale) Moduli di oggetti/librerie                   | Includere msvcrtd. lib e Wmvcore.lib.Do non includere libc. lib o qualsiasi variante.<br/> | Includere Msvcrt. lib e Wmvcore.lib.Do non includere libc. lib o qualsiasi variante.<br/> |



 

Se si usa Microsoft Visual Studio .NET, le impostazioni sono state modificate in posizioni diverse, come illustrato nella tabella seguente. Tutte queste impostazioni sono configurate nella finestra di dialogo **pagine delle proprietà** . Per ottenere la finestra di dialogo, fare clic con il pulsante destro del mouse sul progetto nel riquadro **Esplora soluzioni** e scegliere **Proprietà** dal menu di scelta rapida.



| Impostazione                                                                  | Valore di debug                                                                              | Valore versione                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Proprietà di configurazione/C/C++/generazione di codice) Libreria di runtime     | DLL di debug multi-thread (/MTd)                                                          | DLL multi-thread (/MD)                                                                |
| (Proprietà di configurazione/linker/input) Dipendenze aggiuntive      | Includere msvcrtd. lib e Wmvcore.lib.Do non includere libc. lib o qualsiasi variante.<br/> | Includere Msvcrt. lib e Wmvcore.lib.Do non includere libc. lib o qualsiasi variante.<br/> |
| (Proprietà di configurazione/linker/input) Ignora tutte le librerie predefinite | Sì                                                                                      | Sì                                                                                     |



 

Se si vuole ritardare il caricamento di Wmvcore.dll o di qualsiasi altra DLL, usare l'opzione di collegamento/DELAYLOAD in Microsoft Visual C++ 6,0 o ritardare le DLL caricate in Microsoft Visual C++ .NET.

Inoltre, è necessario includere le directory per le librerie e le intestazioni di Windows Media Format SDK. Per trovare le impostazioni della directory per Visual C++ 6,0, scegliere **Opzioni** dal menu **strumenti** , quindi fare clic sulla scheda **directory** . Quando si usa Visual C++ .NET, scegliere **Opzioni** dal menu **strumenti** , quindi selezionare progetti/directory di VC + + nell'elenco di opzioni. Aggiungere directory come illustrato nella tabella seguente. Se è stata modificata la directory di installazione per Windows Media Format SDK, il percorso sarà diverso.



| Tipo di directory | Percorso predefinito                 |
|----------------|------------------------------|
| File di inclusione  | C: \\ WMSDK \\ WMFSDK11 \\ inclusi |
| File di libreria  | C: \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Se si usa Platform SDK, i percorsi predefiniti verranno visualizzati come segue:



| Tipo di directory | Percorso predefinito                                              |
|----------------|-----------------------------------------------------------|
| File di inclusione  | C: \\ programmi \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ include |
| File di libreria  | C: \\ programmi \\ Microsoft SDsK \\ Windows \\ v 6.0 \\ lib     |



 

Prima di chiamare le funzioni di creazione, è necessario inizializzare COM con una chiamata a **CoInitialize** o **CoinitializeEx**. È possibile utilizzare il modello di threading libero o il modello di threading dell'Apartment, ma il modello di threading dell'Apartment impone restrizioni di threading sull'applicazione. Per ulteriori informazioni su Microsoft Component Object Model (COM), vedere la pagina relativa a COM sul [sito Web Microsoft](../com/the-component-object-model.md).

**Nota** Le applicazioni che svolgono o creano file protetti da Digital Rights Management (DRM) richiedono una libreria statica personalizzata che deve essere ottenuta separatamente da Microsoft. Per ulteriori informazioni, vedere il modulo Windows Media Licensing sul [sito Web Microsoft](https://www.microsoft.com/licensing/default). Se si usa la libreria DRM, è consigliabile non eseguire il collegamento a wmvcore. lib.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](getting-started.md)
</dt> </dl>

 

