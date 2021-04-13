---
title: Funzioni di condivisione
description: Le funzioni di condivisione di gestione della rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5034d46e233ebb7ed4de691bd79942a3ecdf5263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399579"
---
# <a name="share-functions"></a>Funzioni di condivisione

Le funzioni di condivisione di gestione della rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.

Le funzioni di condivisione sono elencate di seguito.



| Funzione                                  | Descrizione                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**Funzione NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Condivide una risorsa in un server.                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Esegue una query sull'eventuale condivisione di un dispositivo da parte di un server.                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Elimina un nome di condivisione dall'elenco di risorse condivise di un server.       |
| [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Recupera le informazioni sulla condivisione di ogni risorsa condivisa in un server.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Recupera le informazioni su una risorsa condivisa specificata in un server. |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Imposta i parametri di una risorsa condivisa.                                 |



 

Queste funzioni di condivisione sono valide solo per le condivisioni in un server di Server Message Block (LAN Manager). Queste funzioni di condivisione non supportano le condivisioni di file system distribuito (DFS). Ad esempio, la funzione [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) può recuperare solo le informazioni per una risorsa di condivisione specificata in un server SMB. Per recuperare le informazioni per una condivisione utilizzando un provider di rete diverso (ad esempio WebDAV o una condivisione DFS), utilizzare la funzione [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) .

La funzione [**funzione NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) consente a un utente o a un'applicazione di condividere una risorsa di un tipo specifico usando il nome di condivisione specificato. La funzione **funzione NetShareAdd** richiede il nome della condivisione e il nome del dispositivo locale per condividere la risorsa. Per accedere alla risorsa, è necessario che un utente o un'applicazione disponga di un account nel server.

È anche possibile specificare un descrittore di sicurezza da associare a una condivisione. I descrittori di sicurezza specificano quali utenti possono accedere ai file attraverso la condivisione e con quale tipo di accesso. Specificare un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con il livello di informazioni [**share \_ info \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) quando si chiama **funzione NetShareAdd** o [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo). **NetShareSetInfo** supporta il livello di informazioni [**condivisione \_ informazioni \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) . Per ulteriori informazioni sui descrittori di sicurezza, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Le funzioni di gestione della rete utilizzano i nomi di condivisione speciali seguenti per la comunicazione interprocesso (IPC) e l'amministrazione remota del server:

-   IPC $, riservata per la comunicazione interprocesso
-   ADMIN $, riservato per l'amministrazione remota
-   Un $, B $, C $ (e altri nomi di disco locale seguiti da un simbolo di dollaro) assegnati a dispositivi disco locali

Per elencare tutte le connessioni effettuate a una risorsa condivisa in un server o per elencare tutte le connessioni stabilite da un determinato computer, chiamare la funzione [**NetConnectionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) . È possibile chiamare **NetConnectionEnum** con le informazioni di [**connessione \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) e i livelli di informazioni di [**connessione \_ \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1) .

Le funzioni di condivisione sono disponibili ai livelli di informazioni seguenti, sebbene alcuni livelli di condivisione siano applicabili solo ad alcune delle funzioni di condivisione:

-   [**Informazioni sulla condivisione \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**Condividi \_ informazioni \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**Condividi \_ informazioni \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**Condividi \_ informazioni \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**Condividi \_ informazioni \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**Condividi \_ informazioni \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**Condividi \_ informazioni \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**Condividi \_ informazioni \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**Condividi \_ informazioni \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**Condividi \_ informazioni \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Per informazioni dettagliate, vedere la documentazione relativa a una funzione di condivisione specifica.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni di condivisione di gestione della rete. Per ulteriori informazioni, vedere [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 