---
description: Uso delle funzioni CryptoAPI per gestire gli archivi certificati e i certificati, gli elenchi di revoche di certificati e gli elenchi di certificati attendibili all'interno di tali archivi.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Gestione dei certificati con archivi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0bfab57522ea8b400ee8d042b5b2cb1ad37fe7c234a291000eb516b11a6be0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425656"
---
# <a name="managing-certificates-with-certificate-stores"></a>Gestione dei certificati con archivi certificati

Nel corso di un periodo di tempo, [*i*](../secgloss/c-gly.md) certificati si accumulano nel computer di un utente. Per gestire questi certificati sono necessari strumenti. [*CryptoAPI*](../secgloss/c-gly.md) fornisce tali strumenti come funzioni per archiviare, recuperare, eliminare, elencare (enumerare) e verificare i certificati. CryptoAPI offre anche i mezzi per allegare certificati ai messaggi.

CryptoAPI offre due categorie principali di funzioni [](../secgloss/c-gly.md)per la gestione dei certificati: funzioni che gestiscono gli archivi certificati e funzioni che funzionano con i [*certificati,*](../secgloss/c-gly.md) elenchi di revoche di certificati (CRL) ed elenchi di certificati attendibili (CCL) all'interno di tali archivi. [](../secgloss/c-gly.md)

Le funzioni che [*gestiscono gli*](../secgloss/c-gly.md) archivi certificati includono funzioni [](../secgloss/e-gly.md)per l'uso di archivi logici o [*virtuali,*](../secgloss/v-gly.md)archivi [*remoti,*](../secgloss/r-gly.md)archivi esterni e archivi che possono essere ricollocati.

I certificati, [*i CRL*](../secgloss/c-gly.md)e [*i CRL*](../secgloss/c-gly.md) possono essere mantenuti e gestiti negli [*archivi certificati*](../secgloss/c-gly.md). Possono essere recuperati da un archivio in cui sono stati resi persistenti per l'uso nei processi di autenticazione.

[*L'archivio certificati è*](../secgloss/c-gly.md) fondamentale per tutte le funzionalità del certificato. I certificati vengono gestiti nell'archivio usando funzioni con un prefisso "Cert". Un archivio certificati tipico è un elenco collegato [*di certificati,*](../secgloss/c-gly.md) come illustrato nella figura seguente.

![archivio certificati](images/certstore1.png)

La figura precedente mostra:

-   Ogni [*archivio certificati*](../secgloss/c-gly.md) ha un puntatore al primo blocco di certificati in tale archivio.
-   Un blocco di certificati include un puntatore ai dati del certificato e un puntatore "successivo" al blocco di certificati successivo nell'archivio.
-   Il puntatore "next" nell'ultimo blocco di certificati è impostato su **NULL.**
-   Il blocco di dati di un certificato contiene il contesto del certificato di sola lettura ed eventuali proprietà estese del certificato.
-   Il blocco di dati di ogni certificato contiene un [*conteggio dei*](../secgloss/r-gly.md) riferimenti che tiene traccia del numero di puntatori al certificato esistente.

I certificati in un [*archivio certificati vengono*](../secgloss/c-gly.md) in genere conservati in un tipo di archiviazione permanente, ad esempio un file su disco o il Registro di sistema. Gli archivi certificati possono anche essere creati e aperti esclusivamente in memoria. Un archivio di memoria fornisce l'archiviazione temporanea dei certificati per l'uso di certificati che non devono essere conservati.

I percorsi di archiviazione aggiuntivi consentono di mantenere e cercare gli archivi in varie parti del Registro di sistema di un computer locale o, con autorizzazioni appropriate impostate, nel Registro di sistema in un computer remoto.

Ogni utente ha un archivio Personale personale in cui vengono archiviati i certificati dell'utente. L'archivio my può essere in uno dei numerosi percorsi fisici, tra cui il Registro di sistema in un computer locale o remoto, un file su disco, un database, un servizio directory, un [*smart card*](../secgloss/s-gly.md)o un altro percorso. Anche se qualsiasi certificato può essere archiviato nell'archivio personale, questo archivio deve essere riservato ai certificati personali di un utente: i certificati usati per la firma e la decrittografia dei messaggi dell'utente.

L'uso dei certificati per l'autenticazione dipende dalla presenza di certificati emessi da un'autorità di certificazione attendibile. I certificati per le autorità di certificazione attendibili vengono in genere mantenuti nell'archivio radice, che è attualmente persistente in una sottochiave del Registro di sistema. Nel contesto CryptoAPI l'archivio radice è protetto e le finestre di dialogo dell'interfaccia utente ricordano all'utente di inserire solo certificati attendibili in tale archivio. In situazioni di rete aziendale, i certificati possono essere inviati (copiati) da un amministratore di sistema dal computer controller di dominio agli archivi radice nei computer client. Questo processo fornisce a tutti i membri di un dominio elenchi di trust simili.

Altri certificati possono essere archiviati [*nell'archivio*](../secgloss/c-gly.md) di sistema dell'autorità di certificazione (CA) o negli archivi basati su file creati dall'utente.

Per elenchi di funzioni per l'uso e la gestione degli archivi certificati, vedere [Funzioni dell'archivio certificati](cryptography-functions.md).

Per un esempio che usa alcune di queste funzioni, vedere Programma C di [esempio: Operazioni dell'archivio certificati](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dello stato di un archivio certificati](managing-a-certificate-store-state.md)
</dt> <dt>

[Uso dei certificati negli archivi certificati](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Collegamenti al certificato](certificate-links.md)
</dt> <dt>

[Archivi di raccolta](collection-stores.md)
</dt> <dt>

[Archivi logici e fisici](logical-and-physical-stores.md)
</dt> <dt>

[Percorsi dell'archivio di sistema](system-store-locations.md)
</dt> <dt>

[Migrazione dell'archivio certificati](certificate-store-migration.md)
</dt> </dl>

 

 
