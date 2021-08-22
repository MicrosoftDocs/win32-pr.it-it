---
title: Windows Controlli
description: Un controllo è una finestra figlio utilizzata da un'applicazione insieme a un'altra finestra per consentire l'interazione dell'utente.
ms.assetid: 0a6eb481-d94e-40c5-afec-46354520f08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bbf1c7ebf33b5665b086b34dd7134cdebadc299f4e2010710ddf4ae519dc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957540"
---
# <a name="windows-controls"></a>Windows Controlli

## <a name="purpose"></a>Scopo

Un controllo è una finestra figlio utilizzata da un'applicazione insieme a un'altra finestra per consentire l'interazione dell'utente. I controlli vengono usati più spesso all'interno delle finestre di dialogo, ma possono essere usati anche in altre finestre. I controlli all'interno delle finestre di dialogo consentono all'utente di digitare testo, scegliere le opzioni e avviare azioni. I controlli in altre finestre forniscono un'ampia gamma di servizi, ad esempio consentire all'utente di scegliere i comandi, visualizzare lo stato e visualizzare e modificare il testo. Questa documentazione descrive i controlli forniti da Windows e gli elementi di programmazione usati per crearli e modificarli.

Per un elenco di tutti i Windows, incluso un collegamento a una panoramica completa e informazioni di riferimento per ogni controllo, vedere [Libreria di controlli](individual-control-info.md).

## <a name="developer-audience"></a>Sviluppatori

I controlli sono progettati per l'uso da sviluppatori C/C++ e finestre di progettazione dell'interfaccia utente. In generale, gli sviluppatori necessitano di un livello moderato di comprensione dei concetti di programmazione dell'interfaccia utente, Windows api e Unicode.

## <a name="run-time-requirements"></a>Requisiti di runtime

Il supporto per i controlli viene fornito da User32.dll e Comctl32.dll. Per altre informazioni, vedere [Versioni comuni dei controlli](common-control-versions.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                             | Descrizione                                                                                                                                     |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli comuni](common-controls-intro.md)<br/>                     | Fornisce informazioni generali comuni a tutti i controlli supportati da Comctl32.dll.<br/>                                      |
| [Controllare i messaggi](control-messages.md)<br/>                               | Illustra come Windows messaggi vengono usati per comunicare con i controlli.<br/>                                                                 |
| [Controlli personalizzati](user-controls-intro.md)<br/>                             | Vengono descritti vari modi per creare controlli personalizzati. <br/>                                                                                 |
| [Sottoclassare i controlli](subclassing-overview.md)<br/>                       | Descrive un modo per personalizzare un controllo modificandone le funzionalità o aggiungendone di nuove. <br/>                                                 |
| [Disegno personalizzato](custom-draw.md)<br/>                                         | Descrive un servizio, fornito da alcuni controlli, che le applicazioni possono usare per personalizzare vari aspetti dell'aspetto del controllo. <br/> |
| [Considerazioni sulla sicurezza: Controlli Windows Microsoft](sec-comctls.md)<br/> | Vengono fornite informazioni sulle considerazioni sulla sicurezza correlate ai controlli Windows sicurezza. <br/>                                                 |
| [Libreria di controlli](individual-control-info.md)<br/>                         | Vengono fornite panoramiche e informazioni di riferimento su ogni controllo supportato da User32.dll e Comctl32.dll.<br/>                            |
| [Informazioni di riferimento generali sul controllo](common-control-reference.md)<br/>              | Fornisce informazioni di riferimento sugli elementi di programmazione applicabili a più controlli, non solo a un controllo specifico.<br/>           |
| [Controllo di Spy v2.0](control-spy.md)<br/>                                    | Descrive Control Spy, uno strumento che consente agli sviluppatori di comprendere i controlli comuni. <br/>                                                     |
| [Stili di visualizzazione](themes-overview.md)<br/>                                   | Descrive come l'aspetto dei controlli può cambiare a seconda dello stile di visualizzazione scelto dall'utente. <br/>                               |
| [Formato di file del tema](themesfileformat-overview.md)<br/>                     | Illustra il formato dei file theme (con estensione theme) usati in Windows 7 e Windows Vista.<br/>                                                    |



 

 

 





