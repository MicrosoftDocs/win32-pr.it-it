---
description: Prima di implementare il codice che protegge le password, è consigliabile analizzare l'ambiente in uso in modo che un utente malintenzionato tenti di penetrare le difese software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Valutazione delle minacce per la password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318962"
---
# <a name="password-threat-assessment"></a>Valutazione delle minacce per la password

Prima di implementare il codice che protegge le password, è consigliabile analizzare l'ambiente in uso in modo che un utente malintenzionato tenti di penetrare le difese software.

Iniziare analizzando la rete o l'architettura del sistema. Ecco alcuni esempi:

-   Il numero di password che devono essere protette. È necessaria una password per accedere al computer locale? Si tratta della stessa password utilizzata per accedere alla rete? Le password vengono propagate a più di un server nella rete? Quante password devono essere gestite?
-   Il tipo di rete, se presente, che verrà utilizzato. La rete è implementata utilizzando un sistema di directory aziendale (ad esempio LDAP) ed è utilizzata l'architettura della relativa password? Sono presenti oggetti che archiviano password non crittografate?
-   Apri rispetto alla rete chiusa. La rete è autonoma o è aperta all'esterno? In caso affermativo, è protetto da un firewall?
-   Accesso remoto. Gli utenti dovranno accedere alla rete da una posizione remota?

Dopo aver analizzato l'architettura di sistema o di rete, è possibile iniziare ad analizzare il modo in cui un utente malintenzionato potrebbe tentare di attaccare. Ecco alcune possibilità:

-   Leggi una password non crittografata dal registro di sistema di un computer.
-   Leggere una password non crittografata nel software.
-   Leggere una password non crittografata dalla tabella codici scambiata del computer.
-   Leggere una password dal registro eventi di un programma.
-   Leggi una password da uno schema del servizio directory Microsoft Active Directory esteso con oggetti che contengono una password in testo non crittografato.
-   Eseguire un debugger in un programma che richiede una password.
-   Indovinare una password. Potrebbero essere utilizzate alcune tecniche. Ad esempio, l'autore dell'attacco potrebbe conoscere alcune informazioni personali relative a un utente e provare a indovinare una password da tali informazioni, ad esempio il nome di un coniuge, un partner o un figlio. In alternativa, è possibile provare un metodo di forza bruta, in cui vengono tentate tutte le combinazioni di lettere, numeri e punteggiatura (possibile solo se vengono usate password brevi).

Il confronto tra le possibili metodologie di attacco con l'architettura di sistema o di rete potrebbe rivelare rischi per la sicurezza. A questo punto, è possibile stabilire un fattore di rischio per ogni rischio e i fattori di rischio possono essere utilizzati per valutare le correzioni.

 

 



