---
description: Uso delle funzioni CryptoAPI per gestire gli archivi certificati e i certificati, gli elenchi di revoche di certificati e gli elenchi di certificati attendibili all'interno di tali archivi.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Gestione dei certificati con archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554018"
---
# <a name="managing-certificates-with-certificate-stores"></a>Gestione dei certificati con archivi certificati

In un periodo di tempo, i [*certificati*](../secgloss/c-gly.md) si accumuleranno sul computer di un utente. Gli strumenti sono necessari per gestire questi certificati. [*CryptoAPI*](../secgloss/c-gly.md) fornisce tali strumenti come funzioni per archiviare, recuperare, eliminare, elencare (enumerare) e verificare i certificati. CryptoAPI fornisce inoltre i mezzi per alleghi i certificati ai messaggi.

CryptoAPI offre due categorie principali di funzioni per la gestione dei certificati: funzioni che gestiscono [*archivi certificati*](../secgloss/c-gly.md)e funzioni che funzionano con i certificati, gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) e gli elenchi di certificati [*attendibili*](../secgloss/c-gly.md) (scopi consentiti) all'interno di tali archivi.

Le funzioni che gestiscono [*archivi certificati*](../secgloss/c-gly.md) includono funzioni per l'utilizzo di [*archivi*](../secgloss/v-gly.md)logici o virtuali, [*archivi remoti*](../secgloss/r-gly.md), [*archivi esterni*](../secgloss/e-gly.md)e archivi che possono essere spostati.

I certificati, i [*CRL*](../secgloss/c-gly.md)e i [*scopi consentiti*](../secgloss/c-gly.md) possono essere conservati e conservati negli [*archivi certificati*](../secgloss/c-gly.md). Possono essere recuperati da un archivio in cui sono stati salvati in maniera permanente per l'uso nei processi di autenticazione.

L' [*archivio certificati*](../secgloss/c-gly.md) è fondamentale per tutte le funzionalità del certificato. I certificati vengono gestiti nell'archivio usando le funzioni con un prefisso "CERT". Un archivio certificati tipico è un elenco collegato di [*certificati*](../secgloss/c-gly.md) , come illustrato nella figura seguente.

![archivio certificati](images/certstore1.png)

Nella figura precedente viene illustrato quanto segue:

-   Ogni [*archivio certificati*](../secgloss/c-gly.md) dispone di un puntatore al primo blocco di certificati nell'archivio.
-   Un blocco di certificati include un puntatore ai dati del certificato e un puntatore "Next" al blocco del certificato successivo nell'archivio.
-   Il puntatore "Next" nell'ultimo blocco certificate è impostato su **null**.
-   Il blocco di dati di un certificato contiene il contesto del certificato di sola lettura ed eventuali proprietà estese del certificato.
-   Il blocco di dati di ogni certificato contiene un [*conteggio dei riferimenti*](../secgloss/r-gly.md) che tiene traccia del numero di puntatori al certificato esistente.

I certificati in un [*archivio certificati*](../secgloss/c-gly.md) vengono in genere conservati in un tipo di archiviazione permanente, ad esempio un file su disco o il registro di sistema. Gli archivi certificati possono anche essere creati e aperti rigorosamente in memoria. Un archivio di memoria fornisce l'archiviazione temporanea dei certificati per l'utilizzo di certificati che non devono essere conservati.

Percorsi di archiviazione aggiuntivi consentono di mantenere e cercare gli archivi in varie parti del registro di sistema di un computer locale o, con le autorizzazioni appropriate, nel registro di sistema in un computer remoto.

Ogni utente dispone di un archivio personale in cui sono archiviati i certificati dell'utente. L'archivio My può trovarsi in una qualsiasi delle numerose posizioni fisiche, incluso il registro di sistema in un computer locale o remoto, un file su disco, un database, un servizio directory, una [*Smart Card*](../secgloss/s-gly.md)o un'altra posizione. Mentre un certificato può essere archiviato nell'archivio personale, questo archivio deve essere riservato ai certificati personali dell'utente, ovvero i certificati utilizzati per la firma e la decrittografia dei messaggi dell'utente.

L'uso di certificati per l'autenticazione dipende dalla presenza di certificati emessi da un'autorità di certificazione attendibile. I certificati per le autorità emittenti di certificati attendibili vengono in genere conservati nell'archivio radice, che è attualmente persistente in una sottochiave del registro di sistema. Nel contesto CryptoAPI l'archivio radice è protetto e le finestre di dialogo dell'interfaccia utente ricordano all'utente di inserire solo certificati attendibili nell'archivio. Nelle situazioni di rete aziendale, i certificati possono essere inseriti (copiati) da un amministratore di sistema dal computer del controller di dominio agli archivi radice nei computer client. Questo processo fornisce tutti i membri di un dominio con elenchi di attendibilità simili.

Altri certificati possono essere archiviati nell'archivio di sistema dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) o negli archivi basati su file creati dall'utente.

Per gli elenchi di funzioni per l'uso e la gestione di archivi certificati, vedere [funzioni dell'archivio certificati](cryptography-functions.md).

Per un esempio in cui vengono usate alcune di queste funzioni, vedere il [programma C di esempio: operazioni sull'archivio certificati](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dello stato di un archivio certificati](managing-a-certificate-store-state.md)
</dt> <dt>

[Utilizzo dei certificati negli archivi certificati](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Collegamenti al certificato](certificate-links.md)
</dt> <dt>

[Archivi della raccolta](collection-stores.md)
</dt> <dt>

[Archivi logici e fisici](logical-and-physical-stores.md)
</dt> <dt>

[Percorsi di archivio di sistema](system-store-locations.md)
</dt> <dt>

[Migrazione dell'archivio certificati](certificate-store-migration.md)
</dt> </dl>

 

 
