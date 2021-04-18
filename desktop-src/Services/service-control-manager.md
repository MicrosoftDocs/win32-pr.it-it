---
description: Gestione controllo servizi viene avviato all'avvio del sistema. Si tratta di un server RPC (Remote Procedure Call), in modo che i programmi di configurazione del servizio e di controllo del servizio possano modificare i servizi in computer remoti.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gestione controllo servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306534"
---
# <a name="service-control-manager"></a>Gestione controllo servizi

Gestione controllo servizi viene avviato all'avvio del sistema. Si tratta di un server RPC (Remote Procedure Call), in modo che i programmi di configurazione del servizio e di controllo del servizio possano modificare i servizi in computer remoti.

Le funzioni del servizio forniscono un'interfaccia per le seguenti attività eseguite da SCM:

-   Gestione del database dei servizi installati.
-   Avvio di servizi e servizi di driver all'avvio del sistema o su richiesta.
-   Enumerazione dei servizi installati e dei servizi del driver.
-   Gestione delle informazioni sullo stato per l'esecuzione dei servizi e dei servizi del driver.
-   Trasmissione di richieste di controllo ai servizi in esecuzione.
-   Bloccare e sbloccare il database del servizio.

Le sezioni seguenti descrivono il controllo SCM in modo più dettagliato:

-   [Database dei servizi installati](database-of-installed-services.md)
-   [Avvio automatico dei servizi](automatically-starting-services.md)
-   [Avvio dei servizi su richiesta](starting-services-on-demand.md)
-   [Elenco di record di servizio](service-record-list.md)
-   [Handle SCM](scm-handles.md)

 

 



