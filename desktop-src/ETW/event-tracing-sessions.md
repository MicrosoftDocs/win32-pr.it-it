---
description: Le sessioni di traccia eventi registrano gli eventi da uno o più provider abilitati da un controller.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sessioni di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce49453881d9106119dab15b64ac0698e9a493f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883073"
---
# <a name="event-tracing-sessions"></a>Sessioni di traccia eventi

Le sessioni di traccia eventi registrano gli eventi da uno o più [provider](providing-events.md) abilitati da un [controller](controlling-event-tracing-sessions.md) . La sessione è inoltre responsabile della gestione e dello scaricamento dei buffer. Il controller definisce la sessione, che in genere include la specifica del nome del file di log e della sessione, il tipo di file di log da usare e la risoluzione del timestamp usato per registrare gli eventi.

La traccia eventi supporta un massimo di 64 sessioni di traccia eventi eseguite simultaneamente. In queste sessioni sono disponibili due sessioni per scopi specifici. Le sessioni rimanenti sono disponibili per l'uso generale. Le due sessioni per scopi speciali sono:

-   Sessione Global Logger
-   Sessione del logger del kernel NT

La sessione di traccia eventi del logger globale registra gli eventi che si verificano nelle fasi iniziali del processo di avvio del sistema operativo, ad esempio quelli generati dai driver di dispositivo. Per informazioni sulla configurazione della sessione di traccia eventi del logger globale, vedere [configurazione e avvio della sessione Global Logger](configuring-and-starting-the-global-logger-session.md).

La sessione di traccia eventi di NT kernel logger registra gli eventi di sistema predefiniti generati dal sistema operativo, ad esempio, i/o del disco o gli eventi di errore di pagina. Per informazioni sulla configurazione della sessione di traccia degli eventi di NT kernel logger, sulla [configurazione e l'avvio della sessione NT kernel logger](configuring-and-starting-the-nt-kernel-logger-session.md).

Per informazioni sulla definizione di una normale sessione di traccia eventi, vedere [configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Supporta solo le sessioni di traccia eventi 32.

 

 



