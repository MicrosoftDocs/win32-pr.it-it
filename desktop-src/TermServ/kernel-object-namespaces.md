---
title: Spazi dei nomi dell'oggetto kernel
description: Servizi Desktop remoto usa più spazi dei nomi per gli oggetti kernel; uno spazio dei nomi globale viene utilizzato principalmente dai servizi nelle applicazioni client/server.
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20680a32c8b35e3fa2f1ab15c732683d424550f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300296"
---
# <a name="kernel-object-namespaces"></a>Spazi dei nomi dell'oggetto kernel

Un server di Servizi Desktop remoto dispone di più spazi dei nomi per gli oggetti kernel denominati seguenti: eventi, semafori, mutex, timer da attendere, oggetti di mapping di file e oggetti processo. Esiste uno spazio dei nomi globale utilizzato principalmente dai servizi nelle applicazioni client/server. Ogni sessione client dispone inoltre di uno spazio dei nomi separato per questi oggetti, ad esempio in Windows Vista.

Gli spazi dei nomi separati della sessione client consentono a più client di eseguire le stesse applicazioni senza interferire tra loro. Per i processi avviati in una sessione client, il sistema usa lo spazio dei nomi della sessione per impostazione predefinita. Tuttavia, questi processi possono utilizzare lo spazio dei nomi globale anteponendo il prefisso "globale \\ " al nome dell'oggetto. Il codice seguente, ad esempio, chiama [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e crea un oggetto evento denominato CSAPP nello spazio dei nomi globale:

> [!Note]  
> Lo spazio dei nomi globale non è disponibile per le app di Windows Store.

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

Per impostazione predefinita, le applicazioni di servizio in un ambiente Servizi Desktop remoto utilizzano lo spazio dei nomi globale.

La sessione zero viene usata solo per i servizi di hosting e non è presente alcuna sessione della console, a differenza delle versioni precedenti di Windows.

Lo spazio dei nomi globale consente ai processi su più sessioni client di comunicare con un'applicazione di servizio. Ad esempio, un'applicazione client/server può utilizzare un oggetto mutex per la sincronizzazione. Il modulo server può creare l'oggetto mutex nello spazio dei nomi globale. Una sessione client può quindi utilizzare il prefisso "globale \\ " per aprire l'oggetto mutex.

Un altro uso dello spazio dei nomi globale è per le applicazioni che usano oggetti denominati per rilevare che è già presente un'istanza dell'applicazione in esecuzione nel sistema in tutte le sessioni. Questo oggetto denominato deve essere creato o aperto nello spazio dei nomi globale anziché nello spazio dei nomi per sessione. Il caso più comune di esecuzione dell'applicazione una volta per sessione è supportato per impostazione predefinita perché l'oggetto denominato viene creato in uno spazio dei nomi per sessione.

Oltre al prefisso "globale \\ ", i processi client possono usare il prefisso "Local \\ " per creare in modo esplicito un oggetto nello spazio dei nomi della sessione. Queste parole chiave fanno distinzione tra maiuscole e minuscole.

Il prefisso "Session \\ " è riservato per l'utilizzo da parte del sistema e non deve essere usato nei nomi di oggetti del kernel.

Il cambio rapido utente viene implementato tramite sessioni di Servizi Desktop remoto. Il primo utente ad accedere usa la sessione uno, l'utente successivo per accedere usa la sessione due e così via. I nomi degli oggetti kernel devono seguire le linee guida descritte per Servizi Desktop remoto in modo che le applicazioni possano supportare più utenti.

La creazione di un oggetto mapping di file nello spazio dei nomi globale, usando [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), da una sessione diversa dalla sessione zero è un'operazione con privilegi. Per questo motivo, un'applicazione in esecuzione in una sessione del server di host sessione Desktop remoto (host sessione Desktop remoto) arbitraria deve avere abilitato [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) per creare correttamente un oggetto mapping di file nello spazio dei nomi globale. Il controllo dei privilegi è limitato alla creazione di oggetti di mapping di file e non si applica all'apertura di quelli esistenti. Se, ad esempio, un servizio o il sistema crea un oggetto di mapping dei file, qualsiasi processo in esecuzione in una sessione può accedere a tale oggetto di mapping dei file, purché l'utente disponga dell'accesso necessario.

 

 