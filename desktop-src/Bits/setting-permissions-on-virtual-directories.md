---
title: Impostazione delle autorizzazioni per le directory virtuali
description: Per motivi di sicurezza, Servizio trasferimento intelligente in background (BITS) non carica i file in una directory virtuale in cui sono abilitati gli script e le autorizzazioni di esecuzione.
ms.assetid: cf5c8b50-066f-431e-8bdf-ed0692219b20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6753c326e926724a57e1905c3fb9fe24e28fdc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046962"
---
# <a name="setting-permissions-on-virtual-directories"></a>Impostazione delle autorizzazioni per le directory virtuali

Per motivi di sicurezza, Servizio trasferimento intelligente in background (BITS) non carica i file in una directory virtuale in cui sono abilitati gli script e le autorizzazioni di esecuzione. Se si carica un file in una directory virtuale in cui sono abilitate queste autorizzazioni, il processo ha esito negativo con un codice di errore di \_ esecuzione del server BG E \_ \_ \_ abilitata.

BITS non richiede che la directory virtuale sia abilitata per la scrittura, pertanto è consigliabile disattivare l'accesso in scrittura alla directory virtuale.

L'utente autenticato (o l'utente anonimo di IIS per l'autenticazione anonima) deve disporre delle autorizzazioni di modifica per la directory fisica a cui viene mappata la directory virtuale. la concessione di autorizzazioni di scrittura non è sufficiente.

## <a name="specifying-permissions-for-notifications"></a>Impostazione delle autorizzazioni per le notifiche

Lo schema di autenticazione specificato per la directory virtuale e l'URL di notifica (vedere la proprietà [BITSServerNotificationURL](bits-iis-extension-properties.md) ) deve essere compatibile. BITS usa lo schema di autenticazione specificato per la directory virtuale per accedere all'URL di notifica. Il processo di caricamento non riesce se BITS non è in grado di accedere all'URL di notifica a causa di un errore di autenticazione.

Se il tipo di notifica (vedere la proprietà [BITSServerNotificationType](bits-iis-extension-properties.md) ) è [per riferimento](using-bits-notification-request-response-headers.md), l'applicazione deve assicurarsi che l'utente abbia accesso al file a cui si fa riferimento (vedere l'intestazione [bits-request-DataFile-Name](notification-protocol-for-server-applications.md) ). BITS imposta gli ACL nel file a cui si fa riferimento su quelli della directory fisica a cui viene mappata la directory virtuale.

> [!Note]  
> L'applicazione notificata deve essere in grado di eseguire il mapping e accedere al file remoto anche se l'URL di notifica viene servito da un server Web che si trova in un computer diverso da quello della directory di caricamento fisica. L'intestazione [bits-request-DataFile-Name](notification-protocol-for-server-applications.md) contiene sempre una specifica del percorso relativa al computer che ospita il componente estensioni BITS. Un'applicazione in esecuzione in un altro computer potrebbe dover convertire il percorso in un percorso UNC prima di accedervi.

 

BITS supporta molte combinazioni di schemi di autenticazione. Tuttavia, è necessario utilizzare lo schema di autenticazione seguente per la directory virtuale e l'URL di notifica corrispondente.

-   Per supportare le notifiche di riferimento, la directory virtuale deve essere configurata per l'utilizzo dell'autenticazione NTLM (Negotiate) se la directory di caricamento fisico (la directory a cui punta la directory virtuale) utilizza uno schema di autenticazione diverso da anonimo. Se la directory di caricamento fisico consente richieste anonime (nessuna autenticazione), la directory virtuale deve abilitare l'anonima (nessuna autenticazione).

    Gli ACL nella directory di caricamento fisica devono essere impostati in modo tale che l'utente autenticato possa leggere i file nella directory a cui punta l'URL di notifica. BITS usa gli ACL della directory di caricamento fisico per impostare gli ACL del file di caricamento temporaneo (l'intestazione [bits-request-DataFile-Name](notification-protocol-for-server-applications.md) contiene il percorso del file temporaneo).

-   Poiché per le notifiche [di valore](using-bits-notification-request-response-headers.md) non è necessario che l'applicazione notificata acceda a un file temporaneo che contiene il contenuto di caricamento, lo schema di autenticazione può essere anonimo o negoziabile (NTLM). L'unico requisito è che l'utente autenticato per la directory virtuale debba essere anche autorizzato ad accedere all'URL di notifica.

## <a name="specifying-permissions-for-remote-shares"></a>Impostazione delle autorizzazioni per le condivisioni remote

Una directory virtuale può puntare a un'unità mappata in un computer diverso o in una condivisione di rete. Se punta a un'unità di rete mappata, le credenziali usate per eseguire il mapping dell'unità dovrebbero avere il controllo completo sulla condivisione remota.

Se la directory virtuale punta a una condivisione di rete, BITS usa le credenziali utente **Connetti come** della directory virtuale per accedere alla condivisione remota. Per accedere a una condivisione remota, è necessario che l'account **Connect As** disponga dei privilegi descritti nella documentazione relativa alla funzione [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) . BITS accede usando i \_ tipi di \_ \_ accesso interattivo batch o LOGON32 \_ di accesso LOGON32. Per l'account utente **Connect As** è necessario Full-Access le autorizzazioni per la condivisione remota; la concessione di autorizzazioni di scrittura non è sufficiente.

Quando la directory di caricamento fisico è mappata a una condivisione di rete, l'identità del chiamante che richiede l'URL di notifica è l'utente di **connessione come** o l'utente autenticato della directory di caricamento fisico (disponibile solo in IIS 6,0 e versioni successive, quando la casella **di controllo Usa sempre le credenziali dell'utente autenticato per la convalida dell'accesso alla risorsa di rete** è selezionata nella finestra **di dialogo Connetti**

 

 