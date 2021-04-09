---
title: Controlli Windows
description: Un controllo è una finestra figlio utilizzata da un'applicazione insieme a un'altra finestra per consentire l'interazione dell'utente.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bf14f3c93f6f38ba787cba463977a4dca9eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044319"
---
# <a name="windows-controls"></a>Controlli Windows

## <a name="purpose"></a>Scopo

Un controllo è una finestra figlio utilizzata da un'applicazione insieme a un'altra finestra per consentire l'interazione dell'utente. I controlli vengono spesso usati nelle finestre di dialogo, ma possono essere usati anche in altre finestre. I controlli all'interno delle finestre di dialogo forniscono all'utente un modo per digitare il testo, scegliere le opzioni e avviare le azioni. I controlli in altre finestre offrono un'ampia gamma di servizi, ad esempio consentendo all'utente di scegliere i comandi, visualizzare lo stato e visualizzare e modificare il testo. Questa documentazione descrive i controlli forniti da Windows e gli elementi di programmazione usati per crearli e modificarli.

Per un elenco di tutti i controlli Windows, incluso un collegamento a una panoramica completa e informazioni di riferimento per ogni controllo, vedere [libreria di controlli](individual-control-info.md).

## <a name="developer-audience"></a>Sviluppatori

I controlli sono progettati per essere utilizzati dagli sviluppatori C/C++ e dalle finestre di progettazione dell'interfaccia utente. In generale, gli sviluppatori necessitano di un livello moderato di informazioni sui concetti di programmazione dell'interfaccia utente, sulla programmazione dell'API Windows e su Unicode.

## <a name="run-time-requirements"></a>Requisiti di runtime

Il supporto per i controlli viene fornito da User32.dll e Comctl32.dll. Per altre informazioni, vedere [versioni del controllo comuni](common-control-versions.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli comuni](common-controls-intro.md)<br/>                     | Vengono fornite informazioni generali comuni a tutti i controlli supportati da Comctl32.dll.<br/>                                      |
| [Messaggi di controllo](control-messages.md)<br/>                               | Viene illustrato il modo in cui i messaggi di Windows vengono utilizzati per comunicare con i controlli.<br/>                                                                 |
| [Controlli personalizzati](user-controls-intro.md)<br/>                             | Descrive vari modi di creare controlli personalizzati. <br/>                                                                                 |
| [Sottoclassi di controlli](subclassing-overview.md)<br/>                       | Viene descritto come personalizzare un controllo modificandone le funzionalità o aggiungendone di nuove. <br/>                                                 |
| [Progetto personalizzato](custom-draw.md)<br/>                                         | Descrive un servizio, fornito da alcuni controlli, che le applicazioni possono utilizzare per personalizzare i vari aspetti dell'aspetto del controllo. <br/> |
| [Considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md)<br/> | Vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows. <br/>                                                 |
| [Libreria di controlli](individual-control-info.md)<br/>                         | Fornisce panoramiche e informazioni di riferimento su ogni controllo supportato da User32.dll e Comctl32.dll.<br/>                            |
| [Riferimento al controllo generale](common-control-reference.md)<br/>              | Fornisce informazioni di riferimento sugli elementi di programmazione che si applicano a più controlli, non solo a un controllo specifico.<br/>           |
| [Controllare Spy v 2.0](control-spy.md)<br/>                                    | Viene descritto il controllo Spy, uno strumento che consente agli sviluppatori di comprendere i controlli comuni. <br/>                                                     |
| [Stili di visualizzazione](themes-overview.md)<br/>                                   | Viene descritto in che modo l'aspetto dei controlli può variare a seconda dello stile di visualizzazione scelto dall'utente. <br/>                               |
| [Formato file tema](themesfileformat-overview.md)<br/>                     | Viene illustrato il formato dei file tema (tema) usati in Windows 7 e Windows Vista.<br/>                                                    |



 

 

 





