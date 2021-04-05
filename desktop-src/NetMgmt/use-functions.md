---
title: Usare le funzioni
description: La gestione di rete usa le funzioni per esaminare e gestire le connessioni (utilizzi) tra workstation e server. Le funzioni di utilizzo sono elencate di seguito.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872866"
---
# <a name="use-functions"></a>Usare le funzioni

La gestione di rete usa le funzioni per esaminare e gestire le connessioni (utilizzi) tra workstation e server. Le funzioni di utilizzo sono elencate di seguito.



| Funzione                               | Descrizione                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una connessione tra un computer locale e un server.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Termina una connessione a una risorsa condivisa.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Elenca tutte le connessioni correnti tra il computer locale e le risorse nei server remoti. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Restituisce informazioni su una connessione a una risorsa condivisa.                              |



 

Questa funzione si applica solo al client Server Message Block (workstation LAN Manager). La funzione **NetUseGetInfo** non supporta le condivisioni di file System distribuito (DFS). Per recuperare le informazioni di connessione per una risorsa condivisa utilizzando un provider di rete diverso (ad esempio WebDAV o una condivisione DFS), utilizzare la funzione [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

Le connessioni si distinguono dalle sessioni: viene stabilita una *sessione* la prima volta che una workstation stabilisce una connessione a una risorsa condivisa nel server. Tutte le connessioni aggiuntive tra la workstation e il server fanno parte della stessa sessione fino al termine della sessione. È possibile effettuare due tipi di connessioni: le connessioni dei nomi di dispositivo (che possono essere esplicite) e le connessioni UNC (Universal Naming Convention), che possono essere esplicite o implicite.

Le *connessioni* vengono eseguite in base ai singoli utenti. Una connessione eseguita da un utente viene eliminata quando l'utente si disconnette. Per questo motivo, le funzioni di utilizzo della gestione di rete sono solo locali, perché una connessione configurata da un utente remoto non sarà accessibile ad altri utenti, anche all'utente che è stato connesso in modo interattivo a tale computer.

La funzione [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) stabilisce una connessione esplicita tra il computer locale e una risorsa condivisa in un server reindirizzando il nome di un dispositivo locale al nome della condivisione di una risorsa server remota ( \\ \\ *ServerName* \\ *ShareName*). Una volta stabilita la connessione al nome di un dispositivo, gli utenti o le applicazioni possono usare la risorsa remota specificando il nome del dispositivo locale.

Le connessioni UNC implicite vengono eseguite dalla funzione responsabile della connessione. Per stabilire una connessione UNC implicita, un'applicazione passa il nome della condivisione di una risorsa a qualsiasi funzione che accetta i percorsi UNC. La funzione accetta il nome UNC e crea una connessione al nome di condivisione specificato. Per tutte le altre richieste sulla connessione è necessario il nome di condivisione completo.

Le funzioni di utilizzo sono disponibili ai livelli di informazioni seguenti:

-   [**USARE le \_ informazioni \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**USARE le \_ informazioni \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**USARE le \_ informazioni \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 