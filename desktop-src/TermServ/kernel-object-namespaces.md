---
title: Spazi dei nomi degli oggetti kernel
description: Servizi Desktop remoto usa più spazi dei nomi per gli oggetti kernel. Uno spazio dei nomi globale viene usato principalmente dai servizi nelle applicazioni client/server.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e1064638844039091dbe93aa1fedc75cb93f4aa1d012f8864e0154673c6cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989081"
---
# <a name="kernel-object-namespaces"></a>Spazi dei nomi degli oggetti kernel

Un server Servizi Desktop remoto dispone di più spazi dei nomi per i seguenti oggetti kernel denominati: eventi, semafori, mutex, timer in attesa, oggetti di mapping di file e oggetti processo. Esiste uno spazio dei nomi globale usato principalmente dai servizi nelle applicazioni client/server. Inoltre, ogni sessione client ha uno spazio dei nomi separato per questi oggetti, ad esempio in Windows Vista.

Gli spazi dei nomi delle sessioni client separati consentono a più client di eseguire le stesse applicazioni senza interferire tra loro. Per i processi avviati in una sessione client, il sistema usa lo spazio dei nomi della sessione per impostazione predefinita. Tuttavia, questi processi possono usare lo spazio dei nomi globale anteponendo il prefisso \\ "Global" al nome dell'oggetto. Ad esempio, il codice seguente chiama [**CreateEvent e**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) crea un oggetto evento denominato CSAPP nello spazio dei nomi globale:

> [!Note]  
> Lo spazio dei nomi globale non è disponibile per le Windows Store.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Le applicazioni di servizio in un Servizi Desktop remoto usano lo spazio dei nomi globale per impostazione predefinita.

La sessione zero viene usata solo per l'hosting dei servizi e non esiste alcuna sessione della console, a differenza delle versioni precedenti di Windows.

Lo spazio dei nomi globale consente ai processi in più sessioni client di comunicare con un'applicazione di servizio. Ad esempio, un'applicazione client/server potrebbe usare un oggetto mutex per la sincronizzazione. Il modulo server può creare l'oggetto mutex nello spazio dei nomi globale. Una sessione client può quindi usare il prefisso \\ "Global" per aprire l'oggetto mutex.

Un altro uso dello spazio dei nomi globale è per le applicazioni che usano oggetti denominati per rilevare che è già presente un'istanza dell'applicazione in esecuzione nel sistema in tutte le sessioni. Questo oggetto denominato deve essere creato o aperto nello spazio dei nomi globale anziché nello spazio dei nomi per sessione. Il caso più comune di esecuzione dell'applicazione una volta per sessione è supportato per impostazione predefinita perché l'oggetto denominato viene creato in uno spazio dei nomi per sessione.

Oltre al prefisso "Global", i processi client possono usare il prefisso "Local" per creare in modo esplicito un oggetto nello spazio \\ \\ dei nomi della sessione. Queste parole chiave fa distinzione tra maiuscole e minuscole.

Il prefisso "Session" è riservato per l'uso da parte del sistema e non \\ deve essere utilizzato nei nomi degli oggetti kernel.

Il cambio utente rapido viene implementato usando le Servizi Desktop remoto utente. Il primo utente che accede usa la prima sessione, l'utente successivo che accede usa la seconda sessione e così via. I nomi degli oggetti kernel devono seguire le linee guida descritte per Servizi Desktop remoto in modo che le applicazioni possano supportare più utenti.

La creazione di un oggetto mapping di file nello spazio dei nomi globale, tramite [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), da una sessione diversa dalla sessione zero è un'operazione privilegiata. Per questo problema, per un'applicazione in esecuzione in una sessione server host sessione Desktop remoto (Host sessione Desktop remoto) arbitraria deve essere abilitato [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) per creare correttamente un oggetto mapping di file nello spazio dei nomi globale. Il controllo dei privilegi è limitato alla creazione di oggetti di mapping dei file e non si applica all'apertura di oggetti esistenti. Ad esempio, se un servizio o il sistema crea un oggetto di mapping di file, qualsiasi processo in esecuzione in qualsiasi sessione può accedere a tale oggetto di mapping di file purché l'utente abbia l'accesso necessario.

 

 