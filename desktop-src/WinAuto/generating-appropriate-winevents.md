---
title: Generazione di eventi WinEvent appropriati
description: Gli sviluppatori server devono assicurarsi che gli eventi WinEvent appropriati siano generati per tutti gli elementi dell'interfaccia utente, inclusi gli elementi dell'interfaccia utente basati su finestre, gli elementi dell'interfaccia utente senza finestra e gli elementi dell'interfaccia utente con comportamenti altamente personalizzati.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e148578f55f59d2827fd13a637baf5139c3f934ddf24059e437185c15349b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860391"
---
# <a name="generating-appropriate-winevents"></a>Generazione di eventi WinEvent appropriati

Gli sviluppatori server devono assicurarsi che gli eventi WinEvent appropriati siano generati per tutti gli elementi dell'interfaccia utente, inclusi gli elementi dell'interfaccia utente basati su finestre, gli elementi dell'interfaccia utente senza finestra e gli elementi dell'interfaccia utente con comportamenti altamente personalizzati.

USER fornisce il supporto WinEvent predefinito per gli elementi dell'interfaccia utente standard basati su **HWND.** Poiché USER genera questi eventi automaticamente, i server devono generare eventi solo per controlli personalizzati, elementi senza finestra o controlli i cui eventi non sono già generati da USER.

Per inviare un evento, i server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passano la costante dell'evento, un ID oggetto e **HWND** per una finestra in grado di rispondere alle richieste client per altre informazioni. Gli eventi che devono essere generati variano in base al tipo di elemento dell'interfaccia utente. Esistono eventi generali che devono essere inviati per tutti i controlli e eventi specifici che devono essere inviati solo per l'elemento dell'interfaccia utente appropriato.

## <a name="general-events"></a>Eventi generali

Gli eventi WinEvent generali possono essere inviati per tutti gli elementi dell'interfaccia utente. Queste includono:

-   [**EVENTO \_ OBJECT \_ CREATE**](event-constants.md) (quando viene creato un oggetto)
-   [**EVENTO \_ OBJECT \_ DESTROY**](event-constants.md) (quando un oggetto viene eliminato)
-   [**EVENTO \_ OBJECT \_ SHOW**](event-constants.md) (quando viene visualizzato un oggetto)
-   [**EVENTO \_ OBJECT \_ HIDE**](event-constants.md) (quando un oggetto è nascosto)

## <a name="specific-events"></a>Eventi specifici

Esistono anche eventi WinEvent specifici che possono essere inviati per un particolare tipo di elemento dell'interfaccia utente. Ad esempio, usare [**EVENT \_ OBJECT \_ SELECTION**](event-constants.md) per i controlli che consentono all'utente di effettuare una selezione, ad esempio una casella di riepilogo.

Per altre informazioni sugli eventi previsti per un particolare tipo di elemento dell'interfaccia utente, vedere le risorse seguenti:

-   [Appendice A: Informazioni di riferimento Interfaccia utente elementi supportati](appendix-a--supported-user-interface-elements-reference.md). Questa appendice include informazioni sugli elementi dell'interfaccia utente generati dal sistema esposti da Microsoft Active Accessibility. La documentazione per ogni controllo include informazioni sugli eventi che possono essere generati dall'elemento dell'interfaccia utente.
-   [Costanti dell'evento](event-constants.md). Questo argomento include informazioni sugli eventi generati dal sistema operativo e dalle applicazioni server.
-   Accessible Event Watcher (AccEvent.exe). Questo strumento mostra gli eventi inviati dall'utente per un particolare elemento dell'interfaccia utente. È possibile usare questo strumento per informazioni sugli eventi previsti per un elemento dell'interfaccia utente. Per altre informazioni, vedere [Accessible Event Watcher](accessible-event-watcher.md).

 

 




