---
title: Generazione di WinEvents appropriati
description: Gli sviluppatori di server devono garantire che vengano generati WinEvents appropriati per tutti gli elementi dell'interfaccia utente, inclusi gli elementi dell'interfaccia utente basati su finestra, gli elementi dell'interfaccia utente senza finestra e gli elementi dell'interfaccia utente con comportamenti altamente personalizzati.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6273411115e908303e863a34908e15ef91b19c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221835"
---
# <a name="generating-appropriate-winevents"></a>Generazione di WinEvents appropriati

Gli sviluppatori di server devono garantire che vengano generati WinEvents appropriati per tutti gli elementi dell'interfaccia utente, inclusi gli elementi dell'interfaccia utente basati su finestra, gli elementi dell'interfaccia utente senza finestra e gli elementi dell'interfaccia utente con comportamenti altamente personalizzati.

L'utente fornisce il supporto WinEvent predefinito per gli elementi dell'interfaccia utente standard basati su **HWND**. Poiché l'utente genera questi eventi automaticamente, i server devono generare eventi solo per controlli personalizzati, elementi privi di finestra o controlli i cui eventi non sono già generati dall'utente.

Per inviare un evento, i server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) e passano la costante dell'evento, un ID oggetto e l' **HWND** per una finestra che può rispondere alle richieste client per ottenere ulteriori informazioni. Gli eventi che devono essere generati variano in base al tipo di elemento dell'interfaccia utente. Sono presenti eventi generali da inviare per tutti i controlli ed eventi specifici che devono essere inviati solo per l'elemento dell'interfaccia utente appropriato.

## <a name="general-events"></a>Eventi generali

È possibile inviare WinEvents generali per tutti gli elementi dell'interfaccia utente. Tra queste sono incluse:

-   [**Evento \_ \_Creazione di oggetti**](event-constants.md) (quando viene creato un oggetto)
-   [**Evento \_ \_Eliminazione di oggetti**](event-constants.md) (quando un oggetto viene eliminato definitivamente)
-   [**Evento \_ \_Mostra oggetto**](event-constants.md) (quando viene visualizzato un oggetto)
-   [**Evento \_ \_Nascondi oggetto**](event-constants.md) (quando un oggetto è nascosto)

## <a name="specific-events"></a>Eventi specifici

Esistono anche WinEvents specifici che possono essere inviati per un particolare tipo di elemento dell'interfaccia utente. Usare, ad esempio, la [**\_ \_ selezione di oggetti evento**](event-constants.md) per i controlli che consentono all'utente di effettuare una selezione, ad esempio una casella di riepilogo.

Per ulteriori informazioni sugli eventi previsti per un particolare tipo di elemento dell'interfaccia utente, vedere le risorse seguenti:

-   [Appendice A: riferimento agli elementi dell'interfaccia utente supportati](appendix-a--supported-user-interface-elements-reference.md). In questa appendice sono incluse informazioni sugli elementi dell'interfaccia utente generati dal sistema esposti da Microsoft Active Accessibility. La documentazione per ogni controllo include informazioni sugli eventi che possono essere generati dall'elemento dell'interfaccia utente.
-   [Costanti dell'evento](event-constants.md). In questo argomento sono incluse informazioni sugli eventi generati dal sistema operativo e dalle applicazioni server.
-   Watcher eventi accessibili (AccEvent.exe). Questo strumento Mostra gli eventi inviati dall'utente per un particolare elemento dell'interfaccia utente. È possibile utilizzare questo strumento per conoscere gli eventi che è possibile prevedere per un elemento dell'interfaccia utente. Per ulteriori informazioni, vedere [monitoraggio eventi accessibile](accessible-event-watcher.md).

 

 




