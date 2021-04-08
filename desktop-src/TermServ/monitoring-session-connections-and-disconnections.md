---
title: Monitoraggio di connessioni e disconnessioni di sessione
description: Per registrare un'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046848"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Monitoraggio di connessioni e disconnessioni di sessione

Per un'applicazione di servizio, ad esempio un'applicazione server di canale virtuale, per monitorare le connessioni e le disconnessioni della sessione, è necessario registrarla con Servizi Desktop remoto. Per registrare l'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave nel percorso seguente:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Componenti aggiuntivi** TerminalServer del controllo CurrentControlSet di sistema del computer locale

La sottochiave può avere qualsiasi nome. Deve avere un valore **reg \_ SZ** , **Name**, che contiene il nome simbolico dell'applicazione.

``` syntax
Name = AddinName
```

La lunghezza massima della sottochiave e del valore di **Name** è 99 caratteri.

La sottochiave deve avere anche un valore **reg \_ DWORD** che indica il tipo di applicazione server.

``` syntax
Type = AddinType
```

*AddinType* deve essere il valore seguente.



| Valore | Significato                               |
|-------|---------------------------------------|
| 3     | Applicazione in modalità utente, spazio sessione. |



 

La registrazione dell'applicazione di servizio ha effetto solo nelle sessioni create dopo l'esecuzione della registrazione.

Per ogni applicazione di servizio registrato, Servizi Desktop remoto segnalerà un set di oggetti evento quando un client si connette o si disconnette dalla sessione. Ogni plug-in di canale virtuale deve registrarsi e creare gli eventi di notifica chiamando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). I nomi di questi oggetti evento rispettano il formato seguente.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddInName* è la stringa specificata nel valore **nome** della sottochiave del registro di sistema in cui è registrata l'applicazione server. La creazione di questi eventi in una sessione ne comporta la creazione in una speciale directory di eventi per sessione. La directory degli eventi offre una maggiore sicurezza impedendo alle applicazioni in altre sessioni di modificare lo stato di questi eventi.

Per controllare se gli eventi di riconnessione e disconnessione vengono ricevuti sul server, è possibile inserire il flag **RemoteControlPersistent** nel registro di sistema nella chiave seguente:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **AddIns** \\ *AddInName*

Il flag Abilita o Disabilita la riconnessione e la disconnessione degli eventi quando una sessione client viene avviata o arrestata. La sintassi del valore **reg \_ DWORD** è la seguente.

``` syntax
RemoteControlPersistent = flag
```

Il valore di *flag* può essere uno o zero. Il valore predefinito è zero. Se impostato su uno, l'applicazione del servizio non riceverà una notifica se la sessione client viene avviata o arrestata. Se è impostato su zero, un evento di riconnessione viene segnalato all'avvio della sessione client e viene segnalato un evento di disconnessione quando la sessione client viene arrestata.

Il formato del nome dell'oggetto evento precedente è ancora supportato in Windows Server 2008 per compatibilità con le versioni precedenti. Si consiglia di usare il formato più recente di Windows Server 2008 perché è più sicuro.

Il formato di evento precedente è il seguente.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddInName* è la stringa specificata nel valore **nome** della sottochiave del registro di sistema in cui è registrata l'applicazione server. *SessionID* è l'identificatore di sessione di una sessione client.

 

 