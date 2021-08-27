---
description: Le sessioni di traccia eventi registrano gli eventi di uno o più provider abilitati da un controller.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sessioni di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083241"
---
# <a name="event-tracing-sessions"></a>Sessioni di traccia eventi

Le sessioni di traccia eventi registrano gli eventi di uno [o più provider](providing-events.md) [abilitati da un controller.](controlling-event-tracing-sessions.md) La sessione è anche responsabile della gestione e dello scaricamento dei buffer. Il controller definisce la sessione, che in genere include la specifica del nome della sessione e del file di log, il tipo di file di log da usare e la risoluzione del timestamp usato per registrare gli eventi.

Traccia eventi supporta un massimo di 64 sessioni di traccia eventi in esecuzione simultaneamente. Di queste sessioni sono disponibili due sessioni per scopi speciali. Le sessioni rimanenti sono disponibili per l'uso generale. Le due sessioni per scopi speciali sono:

-   Sessione globale del logger
-   Sessione del logger del kernel NT

La sessione di traccia degli eventi del logger globale registra gli eventi che si verificano nelle prime fasi del processo di avvio del sistema operativo, ad esempio quelli generati dai driver di dispositivo. Per informazioni sulla configurazione della sessione di traccia degli eventi del logger globale, vedere Configurazione e [avvio della sessione del logger globale](configuring-and-starting-the-global-logger-session.md).

La sessione di traccia degli eventi del kernel NT registra gli eventi di sistema predefiniti generati dal sistema operativo, ad esempio gli eventi di I/O su disco o di errore di pagina. Per informazioni sulla configurazione della sessione di traccia degli eventi di NT Kernel Logger, [vedere Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

Per informazioni sulla definizione di una normale sessione di traccia eventi, vedere [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Supporta solo 32 sessioni di traccia eventi.

 

 



