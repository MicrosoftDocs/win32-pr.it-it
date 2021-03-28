---
description: Le sessioni di traccia eventi registrano gli eventi da uno o più provider.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controllo delle sessioni di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977719"
---
# <a name="controlling-event-tracing-sessions"></a>Controllo delle sessioni di traccia eventi

Le sessioni di traccia eventi registrano gli eventi da uno o più [provider](providing-events.md). Il controller definisce la sessione e Abilita i provider. La definizione della sessione include in genere la specifica del nome del file di log e della sessione, il tipo di file di log da usare e la risoluzione del timestamp usato per registrare gli eventi. I controller possono inoltre aggiornare ed eseguire query sulle sessioni di traccia eventi.

Negli argomenti seguenti viene illustrato come definire e aggiornare una sessione e abilitare i provider di traccia eventi:

-   [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
-   [Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
-   [Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)
-   [Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
-   [Recupero di dati di traccia eventi aggiuntivi](retrieving-additional-event-tracing-data.md)

Per informazioni sullo scaricamento e l'esecuzione di query sulle sessioni, vedere rispettivamente [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa).

Solo gli utenti che eseguono con privilegi amministrativi elevati, gli utenti nel gruppo Performance Log Users e le applicazioni in esecuzione come LocalSystem, LocalService o NetworkService possono controllare le sessioni di traccia eventi. Per concedere a un utente con restrizioni la possibilità di controllare le sessioni di traccia, aggiungerle al gruppo Performance Log Users.

**Windows XP e windows 2000:** Chiunque può controllare una sessione di traccia.

 

 
