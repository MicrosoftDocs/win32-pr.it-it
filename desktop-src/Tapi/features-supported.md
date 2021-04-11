---
description: L'elenco seguente contiene le funzionalità supportate di TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Funzionalità supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226118"
---
# <a name="features-supported"></a>Funzionalità supportate

L'elenco seguente contiene le funzionalità supportate di TAPI MSP.

-   Implementa un MSP che gestisce un singolo indirizzo per ogni istanza del MSP. Più indirizzi like vengono gestiti creando un'istanza più volte del MSP. Questo semplifica notevolmente l'implementazione di MSP e delle classi di base.
-   Implementa tutte le interfacce MSPI, tra cui [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implementa terminali statici pronti per l'uso per audio e video.
-   Implementa classi di base di terminali generiche. Queste classi di base di terminali vengono usate sia dalle implementazioni del terminale statico indicate sopra che dalle implementazioni dei terminali dinamici disponibili in Termmgr.dll. Il MSP può anche usarli per implementare terminali aggiuntivi.
-   USA Terminal Manager per gestire i terminali dinamici. Crea terminali dinamici in un thread di lavoro con un message pump (per liberare le applicazioni console dalla necessità di elaborare i messaggi della finestra per i terminali di rendering video e per semplificare i problemi di sincronizzazione).
-   Supporta le chiamate che usano un grafico di filtro per ogni flusso.
-   Implementa la gestione degli eventi Graph.
-   Usa le API del pool di thread, insieme a un thread di lavoro, per gestire gli eventi.
-   Usa le API di traccia di Windows 2000 (originariamente sviluppate per il progetto di routing) insieme alla logica aggiuntiva per fornire un meccanismo di registrazione generico flessibile che può registrare simultaneamente in qualsiasi combinazione dei seguenti elementi: un debugger in modalità utente o kernel; una finestra della console separata con messaggi di log separati da un componente; un file di log.
-   Viene eseguito a thread libero.

 

 
