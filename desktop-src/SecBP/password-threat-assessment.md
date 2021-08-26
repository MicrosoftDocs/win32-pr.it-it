---
description: Prima di implementare codice che protegga le password, è consigliabile analizzare l'ambiente specifico per i modi in cui un utente malintenzionato potrebbe tentare di penetrare le difese software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Valutazione delle minacce per le password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9042efa524b0503a648a195e77669b19231fec0445c4b0c8347b802b323076
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977151"
---
# <a name="password-threat-assessment"></a>Valutazione delle minacce per le password

Prima di implementare codice che protegga le password, è consigliabile analizzare l'ambiente specifico per i modi in cui un utente malintenzionato potrebbe tentare di penetrare le difese software.

Iniziare analizzando l'architettura di rete o di sistema. Di seguito sono riportati alcuni esempi:

-   Numero di password che devono essere protette. È necessaria una password per accedere al computer locale? Viene usata la stessa password per accedere alla rete? Le password vengono propagate a più di un server nella rete? Quante password devono essere ospitate?
-   Tipo di rete (se presente) che verrà usato. La rete viene implementata usando un sistema di directory aziendale (ad esempio LDAP) e viene usata l'architettura delle password? Sono presenti oggetti che archiviano password non crittografate?
-   Rete aperta o chiusa. La rete è autonoma o aperta all'esterno? In caso contrario, è protetto da un firewall?
-   Accesso remoto. Gli utenti dovranno accedere alla rete da una posizione remota?

Dopo aver analizzato l'architettura di sistema o di rete, è possibile iniziare ad analizzare il modo in cui un utente malintenzionato potrebbe tentare di attaccare il sistema. Ecco alcune possibilità:

-   Leggere una password non crittografata dal Registro di sistema di un computer.
-   Leggere una password non crittografata hard-coded nel software.
-   Leggere una password non crittografata dalla tabella codici scambiata di un computer.
-   Leggere una password dal registro eventi di un programma.
-   Leggere una password da uno schema esteso del servizio directory Microsoft Active Directory con oggetti che contengono una password di testo non crittografato.
-   Eseguire un debugger in un programma che richiede una password.
-   Indovinare una password. È possibile usare una delle diverse tecniche. Ad esempio, l'utente malintenzionato potrebbe conoscere alcune informazioni personali su un utente e provare a indovinare una password da queste informazioni ,ad esempio il nome di un partner/partner o di un figlio. In caso contrario, è possibile provare un metodo di forza bruta, in cui vengono tentate tutte le combinazioni di lettere, numeri e punteggiatura (fattibile solo quando vengono usate password brevi).

Il confronto delle possibili metodologie di attacco con l'architettura di sistema o di rete potrebbe rivelare rischi per la sicurezza. A questo punto, è possibile stabilire un fattore di rischio per ogni rischio e i fattori di rischio possono essere usati per la valutazione delle correzioni.

 

 



