---
description: Le sessioni di traccia eventi registrano gli eventi di uno o più provider.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controllo delle sessioni di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970eb160812991677aac775af60d08458c269152edca4aa2e30cdf30c111d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130661"
---
# <a name="controlling-event-tracing-sessions"></a>Controllo delle sessioni di traccia eventi

Le sessioni di traccia eventi registrano gli eventi di uno o più [provider](providing-events.md). Il controller definisce la sessione e abilita i provider. La definizione della sessione include in genere la specifica del nome della sessione e del file di log, del tipo di file di log da usare e della risoluzione del timestamp usato per registrare gli eventi. I controller possono anche aggiornare ed eseguire query su sessioni di traccia degli eventi.

Negli argomenti seguenti viene illustrato come definire e aggiornare una sessione e come abilitare i provider di traccia eventi:

-   [Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
-   [Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
-   [Configurazione e avvio di una sessione privata del logger](configuring-and-starting-a-private-logger-session.md)
-   [Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
-   [Recupero di dati di traccia eventi aggiuntivi](retrieving-additional-event-tracing-data.md)

Per informazioni sullo scaricamento e l'esecuzione di query sulle sessioni, vedere [**rispettivamente ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e [**QueryAllTraces.**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa)

Solo gli utenti che eseguono con privilegi amministrativi elevati, gli utenti nel gruppo Performance Log Users e le applicazioni in esecuzione come LocalSystem, LocalService o NetworkService possono controllare le sessioni di traccia degli eventi. Per concedere a un utente con restrizioni la possibilità di controllare le sessioni di traccia, aggiungerle al gruppo Performance Log Users.

**Windows XP e Windows 2000:** Chiunque può controllare una sessione di traccia.

 

 
