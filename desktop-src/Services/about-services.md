---
description: Gestione controllo servizi gestisce un database dei servizi installati e dei servizi driver e fornisce un mezzo unificato e sicuro per controllarli.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Informazioni sui servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bcd2058ec8f8de5cbe56a521e2d83919a17532c00dab175d93305edd3684d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126481"
---
# <a name="about-services"></a>Informazioni sui servizi

Gestione [controllo servizi](service-control-manager.md) gestisce un database dei servizi installati e dei servizi driver e fornisce un mezzo unificato e sicuro per controllarli. Il database include informazioni su come deve essere avviato ogni servizio o servizio driver. Consente inoltre agli amministratori di sistema di personalizzare i requisiti di sicurezza per ogni servizio e quindi di controllare l'accesso al servizio.

I tipi di programmi seguenti usano le funzioni fornite da Gestione controllo servizi.



| Tipo                          | Descrizione                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programma di servizio               | Programma che fornisce codice eseguibile per uno o più servizi. I programmi di servizio usano funzioni che si connettono a Gestione controllo servizi e inviano informazioni sullo stato a Gestione controllo servizi.                                                                                                                                                                          |
| Programma di configurazione del servizio | Programma che esegue query o modifica il database dei servizi. I programmi di configurazione del servizio usano funzioni che aprono il database, installano o eliminano i servizi nel database e e modificano la configurazione e i parametri di sicurezza per i servizi installati. I programmi di configurazione del servizio gestiscono sia i servizi che i servizi driver. |
| Programma di controllo del servizio       | Programma che avvia e controlla i servizi e i servizi driver. I programmi di controllo del servizio usano funzioni che inviano richieste a Gestione controllo servizi, che esegue la richiesta.                                                                                                                                                                     |



 

Questa panoramica illustra gli argomenti seguenti:

-   [Gestione controllo servizi](service-control-manager.md)
-   [Programmi di servizio](service-programs.md)
-   [Programmi di configurazione del servizio](service-configuration-programs.md)
-   [Programmi di controllo del servizio](service-control-programs.md)
-   [Account utente del servizio](service-user-accounts.md)
-   [Servizi interattivi](interactive-services.md)
-   [Sicurezza del servizio e diritti di accesso](service-security-and-access-rights.md)
-   [Debug di un servizio](debugging-a-service.md)
-   [Eventi trigger del servizio](service-trigger-events.md)

 

 



