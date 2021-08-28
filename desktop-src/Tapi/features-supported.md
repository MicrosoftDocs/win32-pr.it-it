---
description: L'elenco seguente contiene le funzionalità supportate da TAPI MSP.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Funzionalità supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f0a37664a578bd091ce9972c1979dc7d22f4db33ab2f8eb803bc2c83642f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080511"
---
# <a name="features-supported"></a>Funzionalità supportate

L'elenco seguente contiene le funzionalità supportate da TAPI MSP.

-   Implementa un msp che gestisce un singolo indirizzo per ogni istanza del msp. Più indirizzi simili vengono gestiti creando più istanze di MSP più volte. Questo semplifica notevolmente l'implementazione di MSP e delle classi di base.
-   Implementa tutte le interfacce MSPI, tra cui [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
-   Implementa terminali statici pronti all'uso per audio e video.
-   Implementa classi di base terminali generiche. Queste classi di base dei terminali vengono usate sia dalle implementazioni di terminali statici menzionate in precedenza che dalle implementazioni di terminali dinamici disponibili in Termmgr.dll. Il msp può anche usarli per implementare terminali aggiuntivi.
-   Usa Gestione terminali per gestire i terminali dinamici. Crea terminali dinamici in un thread di lavoro con un message pump (per liberare le applicazioni console dalla necessità di elaborare messaggi di finestra per i terminali di rendering video e semplificare i problemi di sincronizzazione).
-   Supporta le chiamate che usano un grafo di filtro per flusso.
-   Implementa la gestione degli eventi del grafo.
-   Usa le API di pooling di thread, in combinazione con un thread di lavoro, per gestire gli eventi.
-   Usa le API di traccia di Windows 2000 (originariamente sviluppate per il progetto Routing) insieme a logica aggiuntiva per fornire un meccanismo di registrazione flessibile e generico in grado di accedere contemporaneamente a qualsiasi combinazione di: un debugger in modalità utente o kernel. una finestra della console separata con i messaggi di log separati dal componente; un file di log.
-   Esegue a thread libero.

 

 
