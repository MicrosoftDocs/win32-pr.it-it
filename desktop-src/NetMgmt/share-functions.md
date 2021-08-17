---
title: Funzioni di condivisione
description: Le funzioni di condivisione di gestione di rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server, ad esempio una directory del disco, un dispositivo di stampa o un named pipe, accessibile agli utenti e alle applicazioni in rete.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97dc4570c3ef1300322bdf9bd4c9616176e31661319ac77378c61a71667523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064291"
---
# <a name="share-functions"></a>Funzioni di condivisione

Le funzioni di condivisione di gestione di rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server, ad esempio una directory del disco, un dispositivo di stampa o un named pipe, accessibile agli utenti e alle applicazioni in rete.

Le funzioni di condivisione sono elencate di seguito.



| Funzione                                  | Descrizione                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Condivide una risorsa in un server.                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Esegue una query per determinare se un server condivide un dispositivo.                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Elimina un nome di condivisione dall'elenco di risorse condivise di un server.       |
| [**Enumerazione NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Recupera informazioni di condivisione su ogni risorsa condivisa in un server.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Recupera informazioni su una risorsa condivisa specificata in un server. |
| [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Imposta i parametri di una risorsa condivisa.                                 |



 

Queste funzioni di condivisione si applicano solo alle condivisioni in un server Server Message Block (LAN Manager). Queste funzioni di condivisione non supportano file system distribuito (DFS). Ad esempio, la [**funzione NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) può recuperare informazioni solo per una risorsa di condivisione specificata in un server SMB. Per recuperare informazioni per una condivisione usando un provider di rete diverso ,ad esempio WebDAV o una condivisione DFS, usare la [**funzione WNetGetConnection.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona)

La [**funzione NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) consente a un utente o a un'applicazione di condividere una risorsa di un tipo specifico usando il nome di condivisione specificato. La **funzione NetShareAdd** richiede il nome della condivisione e il nome del dispositivo locale per condividere la risorsa. Un utente o un'applicazione deve avere un account nel server per accedere alla risorsa.

È anche possibile specificare un descrittore di sicurezza da associare a una condivisione. I descrittori di sicurezza specificano quali utenti sono autorizzati ad accedere ai file tramite la condivisione e con quale tipo di accesso. Specificare un [**\_ DESCRITTORE DI SICUREZZA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con il livello di informazioni SHARE INFO [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) quando si chiama **NetShareAdd** o [**NetShareSetInfo.**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) **NetShareSetInfo** supporta il [**livello di informazioni SHARE INFO \_ \_ 1501.**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) Per altre informazioni sui descrittori di sicurezza, vedere [Controllo di accesso.](/windows/desktop/SecAuthZ/access-control)

Le funzioni di gestione di rete usano i nomi di condivisione speciali seguenti per la comunicazione interprocesso (IPC) e l'amministrazione remota del server:

-   IPC$, riservato per la comunicazione interprocesso
-   ADMIN$, riservato per l'amministrazione remota
-   A$, B$, C$ (e altri nomi di dischi locali seguiti da un simbolo di dollaro), assegnati ai dispositivi disco locale

Per elencare tutte le connessioni stabilite a una risorsa condivisa in un server o per elencare tutte le connessioni stabilite da un computer specifico, chiamare [**la funzione NetConnectionEnum.**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) È possibile chiamare **NetConnectionEnum** ai [**livelli di informazioni CONNECTION INFO \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) [**e CONNECTION INFO \_ \_ 1.**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1)

Le funzioni di condivisione sono disponibili ai livelli di informazioni seguenti, anche se alcuni livelli di condivisione sono applicabili solo ad alcune delle funzioni di condivisione:

-   [**CONDIVIDI \_ INFORMAZIONI \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**SHARE \_ INFO \_ 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**CONDIVIDI \_ INFORMAZIONI \_ 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**SHARE \_ INFO \_ 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**SHARE \_ INFO \_ 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Per informazioni dettagliate, vedere la documentazione relativa a una funzione di condivisione specifica.

Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni di condivisione di gestione di rete. Per altre informazioni, vedere [**IADsFileShare.**](/windows/desktop/api/iads/nn-iads-iadsfileshare)

 

 