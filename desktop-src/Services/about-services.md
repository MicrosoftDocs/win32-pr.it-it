---
description: Gestione controllo servizi gestisce un database di servizi e driver installati e fornisce un mezzo unificato e sicuro per controllarli.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informazioni sui servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967869"
---
# <a name="about-services"></a>Informazioni sui servizi

[Gestione controllo servizi](service-control-manager.md) gestisce un database di servizi e driver installati e fornisce un mezzo unificato e sicuro per controllarli. Nel database sono incluse informazioni sulla modalità di avvio di ogni servizio o servizio driver. Consente inoltre agli amministratori di sistema di personalizzare i requisiti di sicurezza per ogni servizio e quindi di controllare l'accesso al servizio.

I tipi di programmi seguenti usano le funzioni fornite da SCM.



| Tipo                          | Descrizione                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programma del servizio               | Programma che fornisce codice eseguibile per uno o più servizi. I programmi di servizio utilizzano funzioni che si connettono a SCM e inviano informazioni sullo stato a SCM.                                                                                                                                                                          |
| Programma di configurazione del servizio | Programma che esegue query o modifica il database dei servizi. I programmi di configurazione dei servizi utilizzano funzioni che aprono il database, installano o eliminano i servizi nel database ed eseguono query o modificano i parametri di configurazione e di sicurezza per i servizi installati. I programmi di configurazione dei servizi gestiscono sia servizi che servizi driver. |
| Programma di controllo del servizio       | Programma che avvia e controlla i servizi e i servizi del driver. I programmi di controllo del servizio usano funzioni che inviano richieste a SCM, che esegue la richiesta.                                                                                                                                                                     |



 

In questa panoramica vengono illustrati gli argomenti seguenti:

-   [Gestione controllo servizi](service-control-manager.md)
-   [Programmi di servizio](service-programs.md)
-   [Programmi di configurazione del servizio](service-configuration-programs.md)
-   [Programmi di controllo del servizio](service-control-programs.md)
-   [Account utente del servizio](service-user-accounts.md)
-   [Servizi interattivi](interactive-services.md)
-   [Sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md)
-   [Debug di un servizio](debugging-a-service.md)
-   [Eventi trigger del servizio](service-trigger-events.md)

 

 



