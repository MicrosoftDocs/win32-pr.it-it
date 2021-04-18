---
description: Le funzioni di condivisione di rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Funzioni di condivisione di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310780"
---
# <a name="network-share-functions"></a>Funzioni di condivisione di rete

Le funzioni di condivisione di rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.

Le funzioni di condivisione sono elencate di seguito.



| Funzione                                   | Descrizione                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [**Funzione NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | Condivide una risorsa in un server.                                       |
| [**NetShareCheck**](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | Esegue una query sull'eventuale condivisione di un dispositivo da parte di un server.                        |
| [**NetShareDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | Elimina un nome di condivisione dall'elenco di risorse condivise di un server.       |
| [**NetShareEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | Recupera le informazioni sulla condivisione di ogni risorsa condivisa in un server.  |
| [**NetShareGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | Recupera le informazioni su una risorsa condivisa specificata in un server. |
| [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | Imposta i parametri di una risorsa condivisa.                                 |



 

La funzione [**funzione NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) consente a un utente o a un'applicazione di condividere una risorsa di un tipo specifico usando il nome di condivisione specificato. La funzione **funzione NetShareAdd** richiede il nome della condivisione e il nome del dispositivo locale per condividere la risorsa. Per accedere alla risorsa, è necessario che un utente o un'applicazione disponga di un account nel server.

È anche possibile specificare un descrittore di sicurezza da associare a una condivisione. I descrittori di sicurezza specificano quali utenti possono accedere ai file attraverso la condivisione e con quale tipo di accesso. Specificare un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con il livello di informazioni [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) quando si chiama [**funzione NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) o [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo). **NetShareSetInfo** supporta il livello di informazioni [**condivisione \_ informazioni \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) . Per ulteriori informazioni sui descrittori di sicurezza, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Le funzioni di gestione della rete utilizzano i nomi di condivisione speciali seguenti per la comunicazione interprocesso (IPC) e l'amministrazione remota del server:

-   IPC $, riservata per la comunicazione interprocesso
-   ADMIN $, riservato per l'amministrazione remota
-   Un $, B $, C $ (e altri nomi di disco locale seguiti da un simbolo di dollaro) assegnati a dispositivi disco locali

Per elencare tutte le connessioni effettuate a una risorsa condivisa in un server o per elencare tutte le connessioni stabilite da un determinato computer, chiamare la funzione [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) . È possibile chiamare **NetConnectionEnum** con le informazioni di [**connessione \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) e i livelli di informazioni di [**connessione \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) .

Le funzioni di condivisione sono disponibili ai livelli di informazioni seguenti:

<dl>

[**Informazioni sulla condivisione \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[**Condividi \_ informazioni \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[**Condividi \_ informazioni \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[**Condividi \_ informazioni \_ 501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[**Condividi \_ informazioni \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[**Condividi \_ informazioni \_ 1005**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

I livelli di informazioni seguenti sono validi solo per [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):

<dl>

[**Condividi \_ informazioni \_ 1004**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[**Condividi \_ informazioni \_ 1006**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[**Condividi \_ informazioni \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni di condivisione di gestione della rete. Per ulteriori informazioni, vedere [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 
