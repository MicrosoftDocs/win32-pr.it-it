---
title: Usare le funzioni
description: Le funzioni di gestione della rete esaminano e gestiscono le connessioni (usi) tra workstation e server. Le funzioni di utilizzo sono elencate di seguito.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61019f6c6e2785f03eb4e2e9a47ed1953e14662c5664dca41465bc83d7c683d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779511"
---
# <a name="use-functions"></a>Usare le funzioni

Le funzioni di gestione della rete esaminano e gestiscono le connessioni (usi) tra workstation e server. Le funzioni di utilizzo sono elencate di seguito.



| Funzione                               | Descrizione                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una connessione tra un computer locale e un server.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Termina una connessione a una risorsa condivisa.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Elenca tutte le connessioni correnti tra il computer locale e le risorse nei server remoti. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Restituisce informazioni su una connessione a una risorsa condivisa.                              |



 

Questa funzione si applica solo al client Server Message Block (workstation LAN Manager). La **funzione NetUseGetInfo** non supporta condivisioni file system distribuito (DFS). Per recuperare le informazioni di connessione per una risorsa condivisa usando un provider di rete diverso ,ad esempio WebDAV o una condivisione DFS, usare la [**funzione WNetGetConnection.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona)

Le connessioni sono distinte dalle sessioni: *una sessione* viene stabilita la prima volta che una workstation effettua una connessione a una risorsa condivisa nel server. Tutte le connessioni aggiuntive tra la workstation e il server fanno parte della stessa sessione fino al termine della sessione. È possibile eseguire due tipi di connessioni: connessioni nome dispositivo (che possono essere solo esplicite) e connessioni UNC (Universal-Naming Convention), che possono essere esplicite o implicite.

*Le* connessioni vengono effettuate in base all'utente. Una connessione effettuata da un utente viene eliminata quando l'utente si disconnette. Per questo motivo, le funzioni di gestione della rete sono solo locali, perché una connessione impostata da un utente remoto non sarebbe accessibile ad altri utenti, nemmeno all'utente connesso in modo interattivo al computer.

La [**funzione NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) stabilisce una connessione esplicita tra il computer locale e una risorsa condivisa in un server reindirizzando un nome di dispositivo locale al nome di condivisione di una risorsa del server remoto ( \\ \\ *nomeserver* \\ *sharename*). Dopo aver effettuato una connessione con il nome del dispositivo, gli utenti o le applicazioni possono usare la risorsa remota specificando il nome del dispositivo locale.

Le connessioni UNC implicite vengono effettuate dalla funzione responsabile della connessione. Per stabilire una connessione UNC implicita, un'applicazione passa il nome di condivisione di una risorsa a qualsiasi funzione che accetta percorsi UNC. La funzione accetta il nome UNC e crea una connessione al nome di condivisione specificato. Tutte le altre richieste su questa connessione richiedono il nome completo della condivisione.

Le funzioni di utilizzo sono disponibili ai livelli di informazioni seguenti:

-   [**INFORMAZIONI \_ \_ SULL'USO 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**INFORMAZIONI \_ \_ SULL'USO 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**INFORMAZIONI \_ \_ SULL'USO 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 