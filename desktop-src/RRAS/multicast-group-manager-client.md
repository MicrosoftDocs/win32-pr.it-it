---
title: Client Gestione gruppi multicast
description: Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714065"
---
# <a name="multicast-group-manager-client"></a>Client Gestione gruppi multicast

Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.

L'API MGM viene utilizzata principalmente dai protocolli di routing multicast. Gli sviluppatori di protocolli di routing multicast usano l'API MGM per:

-   Mantieni l'appartenenza al gruppo
-   Controllare la proprietà dell'interfaccia
-   Ricevere notifiche da Gestione gruppi multicast per le richieste di altri protocolli di routing multicast per i dati multicast

Le applicazioni amministrative specifiche che devono monitorare le voci di inoltri multicast (MFE) possono eseguire questa operazione senza aggiungere o rimuovere l'appartenenza al gruppo. Gli sviluppatori di applicazioni amministrative utilizzano funzioni MGM specifiche per esaminare le informazioni in MFE.

> [!Note]  
> I protocolli di routing multicast accedono anche a MFE.

 

Un MFE sta inviando informazioni di cui il gestore del gruppo multicast crea in base all'appartenenza al gruppo. I MFE recuperati dal gestore del gruppo multicast possono fornire informazioni statistiche. Un'applicazione amministrativa può quindi utilizzare queste informazioni per determinare le azioni appropriate. Ad esempio, un'applicazione amministrativa può eseguire azioni basate sul volume di pacchetti in un'interfaccia specifica.

 

 




