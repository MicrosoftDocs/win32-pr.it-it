---
description: CAPICOM usa i certificati digitali per creare firme, crittografare le chiavi di crittografia della sessione durante la creazione di messaggi in busta e decrittografare le chiavi di sessione crittografate quando viene ricevuto un messaggio in busta.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Uso degli archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f687286d40e64e590079d872a0134742d552b66a9926a1febeb5c42ae2ad7566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971613"
---
# <a name="using-certificate-stores"></a>Uso degli archivi certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM usa i [*certificati*](../secgloss/d-gly.md) digitali per creare firme, crittografare le chiavi di crittografia della sessione durante la creazione di messaggi in busta e decrittografare le chiavi di sessione crittografate quando viene ricevuto un messaggio in busta. Per impostazione predefinita, CAPICOM usa i certificati nell'archivio [](../secgloss/d-gly.md) my a cui è associata una chiave privata per la creazione di firme digitali e la decrittografia della chiave di sessione. Nella maggior parte dei casi, un'applicazione non avrebbe mai bisogno di aprire o gestire direttamente un archivio certificati.

Tuttavia, le applicazioni che creano messaggi in busta usano la [*chiave pubblica*](../secgloss/p-gly.md) di ogni destinatario previsto di un messaggio in busta. Queste chiavi vengono recuperate dai certificati dei destinatari previsti. Di conseguenza, per creare messaggi in busta per un gruppo di destinatari previsti, i certificati di tali destinatari verranno raccolti in un archivio certificati.

Nella tabella seguente sono elencati gli archivi certificati standard normalmente persistenti in una stazione utente.



| Archivio        | Descrizione                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Contiene certificati personali. Questi certificati avranno in genere una chiave privata associata.                                                                                                                                                                                                                                                                             |
| Gli altri utenti | Contiene i certificati di quelli da cui l'utente invia in genere messaggi in busta a o da cui riceve messaggi firmati.                                                                                                                                                                                                                                                     |
| Ca e radice  | Contiene i [*certificati delle*](../secgloss/r-gly.md) autorità di certificazione che l'utente considera attendibili per rilasciare certificati ad altri utenti. I certificati in questi archivi vengono in genere forniti con il sistema operativo o dall'amministratore di rete dell'utente. I certificati nell'archivio radice sono in genere autofirmati. |



 

È possibile creare, aprire e rendere persistenti altri archivi CAPICOM CURRENT USER fornendo \_ un nome di archivio diverso come \_ stringa. Se non esiste un archivio con tale nome, viene creato e aperto un archivio vuoto. Se esiste un archivio, viene aperto e tutti i certificati attualmente presenti nell'archivio vengono resi disponibili.

Le sezioni seguenti illustrano esempi per le attività dell'archivio certificati:

-   [Apertura dell'archivio di Active Directory e recupero dei certificati](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Aggiunta di certificati a un archivio certificati](adding-certificates-to-a-certificate-store.md)
-   [Uso di negozi in posizioni diverse](using-stores-in-different-locations.md)
-   [Raccolta e verifica dei certificati](collecting-and-verifying-certificates.md)

 

 
