---
title: Client di Gestione gruppi multicast
description: Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fceda28404e20be5d2c3192b672b1d4e20cb1f95f238f8b561a989c564f6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790424"
---
# <a name="multicast-group-manager-client"></a>Client di Gestione gruppi multicast

Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.

L'API MGM viene usata principalmente dai protocolli di routing multicast. Gli sviluppatori di protocolli di routing multicast usano l'API MGM per:

-   Gestire l'appartenenza ai gruppi
-   Controllare la proprietà dell'interfaccia
-   Ricevere notifiche dal gestore del gruppo multicast relative alle richieste di altri protocolli di routing multicast per i dati multicast

Le applicazioni amministrative specifiche che devono monitorare le voci di inoltro multicast (MFE) possono eseguire questa operazione senza aggiungere o rimuovere l'appartenenza al gruppo. Gli sviluppatori di applicazioni amministrative usano funzioni MGM specifiche per esaminare le informazioni negli MFE.

> [!Note]  
> I protocolli di routing multicast accedono anche agli MFE.

 

Un MFE inoltra le informazioni create dal gestore di gruppi multicast in base all'appartenenza al gruppo. Gli MFE recuperati dal gestore del gruppo multicast possono fornire informazioni statistiche. Un'applicazione amministrativa può quindi usare queste informazioni per determinare le azioni appropriate. Ad esempio, un'applicazione amministrativa può eseguire azioni basate sul volume di pacchetti in un'interfaccia specifica.

 

 




