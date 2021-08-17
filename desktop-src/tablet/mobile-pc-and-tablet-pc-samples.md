---
description: Panoramica degli esempi di codice API (Application Programming Interface) per le sezioni Tablet PC e Windows Touch di Windows SDK.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Esempi di tablet e tocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cf87ca2cc35da58fe05a72436288413af9f72ecff63a1b2418fb071ca5a025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449784"
---
# <a name="tablet-and-touch-samples"></a>Esempi di tablet e tocco

Questa sezione contiene esempi che illustrano come sviluppare applicazioni con C, Microsoft Visual Basic .NET e C++ per usare input \# penna e tocco.

Per impostazione predefinita, gli esempi vengono installati in <system drive> : Programmi Microsoft Tablet PC Platform SDK Samples durante \\ \\ \\ \\ l'installazione di Tablet PC SDK.

> [!Note]  
> Quando si installa Windows SDK, Windows Server SDK o .NET Framework SDK, gli esempi vengono installati nel percorso predefinito per tale SDK specifico.

 

## <a name="available-samples"></a>Esempi disponibili



| Esempio                                                                           | Descrizione                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Riconoscimento avanzato](advanced-recognition-sample.md)                          | Illustra alcune delle funzionalità di riconoscimento più avanzate, ad esempio la scelta del riconoscitore esplicito, i factoid e altro ancora.<br/>                                                                                                                                                             |
| [Modulo attestazioni automatico](auto-claims-form-sample.md)                                  | Illustra l'uso di due controlli input penna: [il controllo InkEdit](/previous-versions/ms552265(v=vs.100)) e il [controllo InkPicture.](/previous-versions/ms583740(v=vs.100))<br/>                                                                                                        |
| [Riconoscimento di base](basic-recognition-sample.md)                                | Illustra come compilare una semplice applicazione di riconoscimento della grafia usando [l'oggetto RecognizerContext.](/previous-versions/ms828542(v=msdn.10))<br/>                                                                                                                     |
| [Sink di evento C++](c---event-sinks-sample.md)                                    | Illustra i modelli in C++ per tutti gli eventi di Tablet Platform, che possono essere sottoclassati o copiati e incollati e usati come codice modello.<br/>                                                                                                                                   |
| [Completamento automatico caratteri](character-autocomplete-sample.md)                      | Illustra come implementare il completamento automatico dei caratteri in giapponese usando le API di riconoscimento.<br/>                                                                                                                                                                                 |
| [Esempio Web di blog ink](ink-blog-web-sample.md)                                   | Illustra come creare un controllo utente gestito con funzionalità di input penna e che ospita tale controllo in Internet Explorer<br/>                                                                                                                                                         |
| [Appunti input penna](ink-clipboard-sample.md)                                        | Viene illustrata l'interoperabilità dell'input penna tramite gli Appunti.<br/>                                                                                                                                                                                                                          |
| [Raccolta input penna](ink-collection-sample.md)                                      | Illustra una semplice Windows form che usa [l'oggetto InkCollector](/previous-versions/ms583683(v=vs.100)) per raccogliere l'input penna.<br/>                                                                                                                                     |
| [Divisore input penna](ink-divider-sample.md)                                            | Illustra come usare [l'oggetto Divider](/previous-versions/ms839398(v=msdn.10)) per eseguire l'analisi dell'input penna.<br/>                                                                                                                                                                            |
| [Cancellazione input penna](ink-erasing-sample.md)                                            | Illustra l'eliminazione di tratti input penna in un'Windows form che usa [l'oggetto InkCollector](/previous-versions/ms583683(v=vs.100)) per raccogliere l'input penna.<br/>                                                                                                             |
| [Hit test input penna](ink-hit-test-sample.md)                                          | Illustra due modi per eseguire l'hit testing dell'input penna.<br/>                                                                                                                                                                                                                                       |
| [Riconoscimento input penna](ink-recognition-sample.md)                                    | Illustra come creare una semplice applicazione di riconoscimento della grafia.<br/>                                                                                                                                                                                                    |
| [Serializzazione input penna](ink-serialization-sample.md)                                | Illustra come serializzare l'input penna nel formato ISF (Ink Serialized Format).<br/>                                                                                                                                                                                                           |
| [Esempio di controllo Web Ink](ink-web-control-sample.md)                             | Illustra come creare un controllo Ink da usare in un Web browser.<br/>                                                                                                                                                                                                             |
| [Zoom input penna](ink-zoom-sample.md)                                                  | Illustra come eseguire correttamente lo zoom dell'input penna in un'applicazione.<br/>                                                                                                                                                                                                                        |
| [Esempio di più riconoscitori](multiple-recognizers-sample.md)                   | Illustra come eseguire una selezione da un'ampia gamma di riconoscitori installati e quindi usare lo strumento di riconoscimento selezionato.<br/>                                                                                                                                                                        |
| [Esempio Web di distribuzione senza tocco](no-touch-deployment-web-sample.md)             | Illustra come usare [l'oggetto PenInputPanel per](/previous-versions/aa514041(v=msdn.10)) rendere più semplice l'input di testo nelle applicazioni forms. Estende l'esempio di modulo attestazioni auto.<br/>                                                                                      |
| [Peninputpanel](peninputpanel-sample.md)                                        | Illustra come usare [l'oggetto PenInputPanel per](/previous-versions/aa514041(v=msdn.10)) rendere più semplice l'input di testo nelle applicazioni forms. Estende l'esempio di modulo attestazioni auto.<br/>                                                                                      |
| [Esempio di raccolta input penna RealTimeStylus](realtimestylus-ink-collection-sample.md) | Illustra la raccolta di input penna con RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Esempio di plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)               | Illustra l'uso di RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Esempio di modulo cartaceo digitalizzato](scanned-paper-form-sample.md)                       | Illustra l'uso di un form analizzato come bitmap e specificato come immagine di sfondo per un [controllo InkPicture](/previous-versions/ms583740(v=vs.100)) nella parte superiore di un form. Sono state abilitate diverse aree per la raccolta di input penna (o specificate come "input penna").<br/> |
| [Esempio di informazioni sulla piattaforma Tablet PC](tablet-pc-platform-info-sample.md)             | Illustra l'uso della funzione API GetSystemMetrics() Windows per determinare se l'applicazione è in esecuzione in un Tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello di esempio di DLL di riconoscimento](recognizer-dll-sample-template.md)
</dt> </dl>

 

