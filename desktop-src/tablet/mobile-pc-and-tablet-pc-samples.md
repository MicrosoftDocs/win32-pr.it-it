---
description: Panoramica degli esempi di codice di Application Programming Interface (API) per le sezioni Tablet PC e Windows Touch del Windows SDK.
ms.assetid: 4ede7d0e-e826-4b3a-8a46-0f3162c19cb0
title: Esempi di Tablet e touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8562dcc1baa42f44d6ca675344d658b1bf693cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885574"
---
# <a name="tablet-and-touch-samples"></a>Esempi di Tablet e touch

Questa sezione contiene esempi che illustrano come sviluppare applicazioni con C \# , Microsoft Visual Basic .NET e C++ per lavorare con l'input penna e il tocco.

Per impostazione predefinita, gli esempi vengono installati in <system drive> : \\ programmi \\ Microsoft Tablet PC Platform SDK \\ Samples \\ durante l'installazione di Tablet PC SDK.

> [!Note]  
> Quando si installano i Windows SDK, Windows Server SDK o SDK .NET Framework, gli esempi vengono installati nel percorso predefinito per quel particolare SDK.

 

## <a name="available-samples"></a>Esempi disponibili



| Esempio                                                                           | Descrizione                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Riconoscimento avanzato](advanced-recognition-sample.md)                          | Vengono illustrate alcune delle funzionalità di riconoscimento più avanzate, ad esempio la scelta esplicita del riconoscimento, factoids e altro ancora.<br/>                                                                                                                                                             |
| [Modulo Claims automatico](auto-claims-form-sample.md)                                  | Viene illustrato l'utilizzo di due controlli Ink: il controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) e il controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) .<br/>                                                                                                        |
| [Riconoscimento di base](basic-recognition-sample.md)                                | Viene illustrato come compilare una semplice applicazione di riconoscimento della grafia utilizzando l'oggetto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) .<br/>                                                                                                                     |
| [Sink di evento C++](c---event-sinks-sample.md)                                    | Vengono illustrati i modelli in C++ per tutti gli eventi della piattaforma Tablet, che possono essere sottoclassati o copiati e incollati e utilizzati come codice del modello.<br/>                                                                                                                                   |
| [Completamento automatico caratteri](character-autocomplete-sample.md)                      | Viene illustrato come implementare il completamento automatico dei caratteri in giapponese usando le API di riconoscimento.<br/>                                                                                                                                                                                 |
| [Esempio di Web Ink Blog](ink-blog-web-sample.md)                                   | Viene illustrato come creare un controllo utente gestito con funzionalità Inking e ospitare tale controllo in Internet Explorer<br/>                                                                                                                                                         |
| [Appunti input penna](ink-clipboard-sample.md)                                        | Viene illustrata l'interoperabilità dell'input penna mediante gli Appunti.<br/>                                                                                                                                                                                                                          |
| [Raccolta di input penna](ink-collection-sample.md)                                      | Viene illustrata una semplice applicazione Windows Form che utilizza l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per raccogliere input penna.<br/>                                                                                                                                     |
| [Divisore input penna](ink-divider-sample.md)                                            | Viene illustrato come utilizzare l'oggetto [divisore](/previous-versions/ms839398(v=msdn.10)) per eseguire l'analisi dell'input penna.<br/>                                                                                                                                                                            |
| [Cancellazione di input penna](ink-erasing-sample.md)                                            | Viene illustrata l'eliminazione dei tratti di input penna in un'applicazione Windows Form che utilizza l'oggetto [InkCollector](/previous-versions/ms583683(v=vs.100)) per raccogliere input penna.<br/>                                                                                                             |
| [Hit test input penna](ink-hit-test-sample.md)                                          | Vengono illustrati due modi per eseguire l'hit test dell'input penna.<br/>                                                                                                                                                                                                                                       |
| [Riconoscimento input penna](ink-recognition-sample.md)                                    | Viene illustrato come creare una semplice applicazione di riconoscimento della grafia.<br/>                                                                                                                                                                                                    |
| [Serializzazione dell'input penna](ink-serialization-sample.md)                                | Viene illustrato come serializzare l'input penna nel formato ISF (Ink Serialized Format).<br/>                                                                                                                                                                                                           |
| [Esempio di controllo Web Ink](ink-web-control-sample.md)                             | Viene illustrato come creare un controllo Ink da utilizzare in un Web browser.<br/>                                                                                                                                                                                                             |
| [Zoom a penna](ink-zoom-sample.md)                                                  | Viene illustrato come ingrandire correttamente l'input penna in un'applicazione.<br/>                                                                                                                                                                                                                        |
| [Esempio di più riconoscitori](multiple-recognizers-sample.md)                   | Viene illustrato come scegliere da un'ampia gamma di sistemi di riconoscimento installati e quindi utilizzare il riconoscimento selezionato.<br/>                                                                                                                                                                        |
| [Esempio Web di distribuzione senza tocco](no-touch-deployment-web-sample.md)             | Viene illustrato come utilizzare l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per semplificare l'input di testo nelle applicazioni Form. Estende l'esempio di modulo delle attestazioni automatiche.<br/>                                                                                      |
| [PenInputPanel](peninputpanel-sample.md)                                        | Viene illustrato come utilizzare l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per semplificare l'input di testo nelle applicazioni Form. Estende l'esempio di modulo delle attestazioni automatiche.<br/>                                                                                      |
| [Esempio di raccolta inchiostro RealTimeStylus](realtimestylus-ink-collection-sample.md) | Viene illustrata la raccolta di input penna mediante RealTimeStylus.<br/>                                                                                                                                                                                                                           |
| [Esempio di plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)               | Viene illustrato l'utilizzo di RealTimeStylus.<br/>                                                                                                                                                                                                                                       |
| [Esempio di modulo cartaceo analizzato](scanned-paper-form-sample.md)                       | Viene illustrato l'utilizzo di un form analizzato come bitmap e specificato come immagine di sfondo per un controllo [InkPicture](/previous-versions/ms583740(v=vs.100)) sulla parte superiore di un form. Sono state abilitate diverse aree per la raccolta di input penna (o, specificate come "inkable").<br/> |
| [Esempio di informazioni sulla piattaforma Tablet PC](tablet-pc-platform-info-sample.md)             | Viene illustrato l'utilizzo della funzione API Windows GetSystemMetrics () per determinare se l'applicazione è in esecuzione in un Tablet PC.<br/>                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello di esempio della DLL di riconoscimento](recognizer-dll-sample-template.md)
</dt> </dl>

 

