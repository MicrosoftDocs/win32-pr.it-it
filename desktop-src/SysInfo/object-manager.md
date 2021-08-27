---
description: Un oggetto è costituito da un'intestazione standard e attributi specifici dell'oggetto. Poiché tutti gli oggetti hanno la stessa struttura, esiste un singolo gestore di oggetti Windows che gestisce tutti gli oggetti.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gestione oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885349"
---
# <a name="object-manager"></a>Gestione oggetti

Un oggetto è costituito da un'intestazione standard e attributi specifici dell'oggetto. Poiché tutti gli oggetti hanno la stessa struttura, esiste un singolo gestore di oggetti Windows che gestisce tutti gli oggetti.

L'intestazione dell'oggetto include elementi come il nome dell'oggetto, in modo che altri processi possano fare riferimento all'oggetto in base al nome e un descrittore di sicurezza, in modo che il gestore di oggetti possa controllare quali processi accedono alla risorsa di sistema.

Di seguito sono riportate le attività eseguite dal gestore oggetti:

-   Creazione di oggetti
-   Verifica che un processo abbia il diritto di usare l'oggetto
-   Creazione di handle di oggetto e restituzione al chiamante
-   Gestione delle quote delle risorse
-   Creazione di handle duplicati
-   Handle di chiusura per gli oggetti

 

 



