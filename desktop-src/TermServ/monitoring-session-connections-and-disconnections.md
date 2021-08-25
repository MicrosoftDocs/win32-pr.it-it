---
title: Monitoraggio delle connessioni e delle disconnessioni delle sessioni
description: Per registrare un'applicazione Servizi Desktop remoto, archiviare il nome dell'applicazione server del canale virtuale nel Registro di sistema aggiungendo una sottochiave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2813399650d535d10864f384afb6b745fb9e50039f2b981df61ceb2e6452a608
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989101"
---
# <a name="monitoring-session-connections-and-disconnections"></a>Monitoraggio delle connessioni e delle disconnessioni delle sessioni

Per un'applicazione di servizio, ad esempio un'applicazione server del canale virtuale, per monitorare le connessioni di sessione e le disconnessioni, è necessario registrarla con Servizi Desktop remoto. Per registrare l'applicazione Servizi Desktop remoto, archiviare il nome dell'applicazione server del canale virtuale nel Registro di sistema aggiungendo una sottochiave nel percorso seguente:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addins**

La sottochiave può avere qualsiasi nome. Deve avere un valore **REG \_ SZ,** **Name**, che contiene il nome simbolico dell'applicazione.

``` syntax
Name = AddinName
```

La lunghezza massima della sottochiave e del valore di **Name** è di 99 caratteri.

La sottochiave deve anche avere un **valore \_ REG DWORD** che indica il tipo di applicazione server.

``` syntax
Type = AddinType
```

*AddinType* deve essere il valore seguente.



| Valore | Significato                               |
|-------|---------------------------------------|
| 3     | Applicazione in modalità utente, spazio della sessione. |



 

La registrazione dell'applicazione di servizio viene eseguita solo nelle sessioni create dopo l'esecuzione della registrazione.

Per ogni applicazione di servizio registrata, Servizi Desktop remoto segnalerà un set di oggetti evento quando un client si connette o si disconnette dalla sessione. Ogni plug-in del canale virtuale deve registrarsi e creare gli eventi di notifica chiamando [**CreateEvent.**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) I nomi di questi oggetti evento sono conformi al formato seguente.

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

*AddinName è* la stringa specificata nel valore **Name** della sottochiave del Registro di sistema in cui è registrata l'applicazione server. La creazione di questi eventi in una sessione ne determina la creazione in una speciale directory di eventi per sessione. La directory degli eventi offre una sicurezza superiore impedendo alle applicazioni in altre sessioni di modificare lo stato di questi eventi.

Per controllare se gli eventi RECONNECT e DISCONNECT vengono ricevuti nel server, è possibile inserire il flag **RemoteControlPersistent** nel Registro di sistema sotto la chiave seguente:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **Addins** \\ *addinname*

Il flag abilita o disabilita la segnalazione degli eventi RECONNECT e DISCONNECT all'avvio o all'arresto di una sessione client. La sintassi del **valore \_ DWORD REG** è la seguente.

``` syntax
RemoteControlPersistent = flag
```

Il valore del *flag* può essere uno o zero. Zero è il valore predefinito. Se impostato su uno, l'applicazione di servizio non riceverà una notifica se la sessione client viene avviata o arrestata. Se impostato su zero, all'avvio della sessione client viene segnalato un evento RECONNECT e un evento DISCONNECT all'arresto della sessione client.

Il formato del nome dell'oggetto evento precedente è ancora supportato in Windows Server 2008 per la compatibilità con le versioni precedenti. È consigliabile usare la versione più recente Windows Server 2008 perché è più sicura.

Il formato dell'evento precedente è il seguente.

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

*AddinName è* la stringa specificata nel valore **Name** della sottochiave del Registro di sistema in cui è registrata l'applicazione server. *SessionId è* l'identificatore di sessione di una sessione client.

 

 