---
description: Un oggetto è costituito da un'intestazione standard e da attributi specifici dell'oggetto. Poiché tutti gli oggetti hanno la stessa struttura, in Windows è disponibile un singolo gestore di oggetti che gestisce tutti gli oggetti.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gestore oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967995"
---
# <a name="object-manager"></a>Gestore oggetti

Un oggetto è costituito da un'intestazione standard e da attributi specifici dell'oggetto. Poiché tutti gli oggetti hanno la stessa struttura, in Windows è disponibile un singolo gestore di oggetti che gestisce tutti gli oggetti.

L'intestazione dell'oggetto include elementi come il nome dell'oggetto, in modo che altri processi possano fare riferimento all'oggetto in base al nome e a un descrittore di sicurezza, in modo che il gestore di oggetti possa controllare i processi che accedono alla risorsa di sistema.

Le attività eseguite dal gestore di oggetti includono quanto segue:

-   Creazione di oggetti
-   Verifica per verificare se un processo ha il diritto di usare l'oggetto
-   Creazione di handle di oggetto e relativa restituzione al chiamante
-   Gestione delle quote delle risorse
-   Creazione di handle duplicati
-   Chiusura di handle per gli oggetti

 

 



