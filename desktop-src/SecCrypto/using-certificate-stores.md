---
description: CAPICOM usa i certificati digitali per creare firme, crittografare le chiavi di crittografia della sessione durante la creazione di messaggi in busta e decrittografare le chiavi della sessione crittografata quando viene ricevuto un messaggio in busta.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Uso degli archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308640"
---
# <a name="using-certificate-stores"></a>Uso degli archivi certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM usa i [*certificati digitali*](../secgloss/d-gly.md) per creare firme, crittografare le chiavi di crittografia della sessione durante la creazione di messaggi in busta e decrittografare le chiavi della sessione crittografata quando viene ricevuto un messaggio in busta. Per impostazione predefinita, CAPICOM usa i certificati nell'archivio My che dispongono di una chiave privata associata per la creazione e la decrittografia della chiave di sessione per le [*firme digitali*](../secgloss/d-gly.md) . Nella maggior parte dei casi, un'applicazione non deve mai aprire o gestire in altro modo direttamente un archivio certificati.

Tuttavia, le applicazioni che creano messaggi in busta digitale utilizzano la [*chiave pubblica*](../secgloss/p-gly.md) di ogni destinatario previsto di un messaggio in busta digitale. Queste chiavi vengono recuperate dai certificati dei destinatari desiderati. Pertanto, per creare messaggi in busta per un gruppo di destinatari desiderati, i certificati di tali destinatari vengono raccolti in un archivio certificati.

La tabella seguente elenca gli archivi certificati standard normalmente salvati in modo permanente in una stazione utente.



| Archivio        | Descrizione                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Contiene certificati personali. A questi certificati sarà in genere associata una chiave privata.                                                                                                                                                                                                                                                                             |
| Gli altri utenti | Contiene i certificati di quelli che l'utente invia in genere i messaggi in busta o riceve i messaggi firmati da.                                                                                                                                                                                                                                                     |
| CA e radice  | Contiene i [*certificati*](../secgloss/r-gly.md) delle autorità di certificazione che l'utente considera attendibile per emettere certificati ad altri. I certificati in questi archivi vengono in genere forniti con il sistema operativo o dall'amministratore di rete dell'utente. I certificati nell'archivio radice sono in genere autofirmati. |



 

\_ \_ È possibile creare, aprire e salvare in modo permanente gli archivi utente correnti di CAPICOM assegnando un nome di archivio diverso sotto forma di stringa. Se non esiste un archivio con tale nome, viene creato e aperto un archivio vuoto. Se un archivio esiste, viene aperto e tutti i certificati attualmente presenti nell'archivio vengono resi disponibili.

Le sezioni seguenti illustrano esempi per le attività dell'archivio certificati:

-   [Apertura dell'archivio Active Directory e recupero dei certificati](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Aggiunta di certificati a un archivio certificati](adding-certificates-to-a-certificate-store.md)
-   [Uso di archivi in posizioni diverse](using-stores-in-different-locations.md)
-   [Raccolta e verifica dei certificati](collecting-and-verifying-certificates.md)

 

 
