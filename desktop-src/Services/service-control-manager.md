---
description: Gestione controllo servizi viene avviato all'avvio del sistema. Si tratta di un server RPC (Remote Procedure Call), in modo che la configurazione del servizio e i programmi di controllo dei servizi possano modificare i servizi nei computer remoti.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gestione controllo servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37d651a96f9685fa82b5ea92ebb3a0b72d80bfc62cd0db80729ec1cb95acc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889034"
---
# <a name="service-control-manager"></a>Gestione controllo servizi

Gestione controllo servizi viene avviato all'avvio del sistema. Si tratta di un server RPC (Remote Procedure Call), in modo che la configurazione del servizio e i programmi di controllo dei servizi possano modificare i servizi nei computer remoti.

Le funzioni del servizio forniscono un'interfaccia per le attività seguenti eseguite da Gestione controllo servizi:

-   Gestione del database dei servizi installati.
-   Avvio dei servizi e dei driver all'avvio del sistema o su richiesta.
-   Enumerazione dei servizi installati e dei servizi driver.
-   Gestione delle informazioni sullo stato per l'esecuzione di servizi e servizi driver.
-   Trasmissione delle richieste di controllo ai servizi in esecuzione.
-   Blocco e sblocco del database del servizio.

Le sezioni seguenti descrivono SCM in modo più dettagliato:

-   [Database dei servizi installati](database-of-installed-services.md)
-   [Avvio automatico dei servizi](automatically-starting-services.md)
-   [Avvio di servizi su richiesta](starting-services-on-demand.md)
-   [Elenco di record del servizio](service-record-list.md)
-   [Handle SCM](scm-handles.md)

 

 



