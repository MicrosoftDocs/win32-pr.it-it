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
# <a name="managing-certificates-with-certificate-stores"></a><span data-ttu-id="1ad4a-103">Gestione dei certificati con archivi certificati</span><span class="sxs-lookup"><span data-stu-id="1ad4a-103">Managing Certificates with Certificate Stores</span></span>

<span data-ttu-id="1ad4a-104">In un periodo di tempo, i [*certificati*](../secgloss/c-gly.md) si accumuleranno sul computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-104">Over a period of time, [*certificates*](../secgloss/c-gly.md) will accumulate on a user's computer.</span></span> <span data-ttu-id="1ad4a-105">Gli strumenti sono necessari per gestire questi certificati.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-105">Tools are required to manage these certificates.</span></span> <span data-ttu-id="1ad4a-106">[*CryptoAPI*](../secgloss/c-gly.md) fornisce tali strumenti come funzioni per archiviare, recuperare, eliminare, elencare (enumerare) e verificare i certificati.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-106">[*CryptoAPI*](../secgloss/c-gly.md) provides those tools as functions to store, retrieve, delete, list (enumerate), and verify certificates.</span></span> <span data-ttu-id="1ad4a-107">CryptoAPI fornisce inoltre i mezzi per alleghi i certificati ai messaggi.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-107">CryptoAPI also provides the means to attach certificates to messages.</span></span>

<span data-ttu-id="1ad4a-108">CryptoAPI offre due categorie principali di funzioni per la gestione dei certificati: funzioni che gestiscono [*archivi certificati*](../secgloss/c-gly.md)e funzioni che funzionano con i certificati, gli [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL) e gli elenchi di certificati [*attendibili*](../secgloss/c-gly.md) (scopi consentiti) all'interno di tali archivi.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-108">CryptoAPI offers two main categories of functions for managing certificates: functions that manage [*certificate stores*](../secgloss/c-gly.md), and functions that work with the certificates, [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) within those stores.</span></span>

<span data-ttu-id="1ad4a-109">Le funzioni che gestiscono [*archivi certificati*](../secgloss/c-gly.md) includono funzioni per l'utilizzo di [*archivi*](../secgloss/v-gly.md)logici o virtuali, [*archivi remoti*](../secgloss/r-gly.md), [*archivi esterni*](../secgloss/e-gly.md)e archivi che possono essere spostati.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-109">The functions that manage [*certificate stores*](../secgloss/c-gly.md) include functions for working with logical or [*virtual stores*](../secgloss/v-gly.md), [*remote stores*](../secgloss/r-gly.md), [*external stores*](../secgloss/e-gly.md), and stores that can be relocated.</span></span>

<span data-ttu-id="1ad4a-110">I certificati, i [*CRL*](../secgloss/c-gly.md)e i [*scopi consentiti*](../secgloss/c-gly.md) possono essere conservati e conservati negli [*archivi certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1ad4a-110">Certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can be kept and maintained in [*certificate stores*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="1ad4a-111">Possono essere recuperati da un archivio in cui sono stati salvati in maniera permanente per l'uso nei processi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-111">They can be retrieved from a store where they have been persisted for use in authentication processes.</span></span>

<span data-ttu-id="1ad4a-112">L' [*archivio certificati*](../secgloss/c-gly.md) è fondamentale per tutte le funzionalità del certificato.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-112">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate functionality.</span></span> <span data-ttu-id="1ad4a-113">I certificati vengono gestiti nell'archivio usando le funzioni con un prefisso "CERT".</span><span class="sxs-lookup"><span data-stu-id="1ad4a-113">The certificates are managed in the store using functions with a "Cert" prefix.</span></span> <span data-ttu-id="1ad4a-114">Un archivio certificati tipico è un elenco collegato di [*certificati*](../secgloss/c-gly.md) , come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-114">A typical certificate store is a linked list of [*certificates*](../secgloss/c-gly.md) as shown in the following illustration.</span></span>

![archivio certificati](images/certstore1.png)

<span data-ttu-id="1ad4a-116">Nella figura precedente viene illustrato quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1ad4a-116">The preceding illustration shows:</span></span>

-   <span data-ttu-id="1ad4a-117">Ogni [*archivio certificati*](../secgloss/c-gly.md) dispone di un puntatore al primo blocco di certificati nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-117">Each [*certificate store*](../secgloss/c-gly.md) has a pointer to the first certificate block in that store.</span></span>
-   <span data-ttu-id="1ad4a-118">Un blocco di certificati include un puntatore ai dati del certificato e un puntatore "Next" al blocco del certificato successivo nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-118">A certificate block includes a pointer to that certificate's data and a "next" pointer to the next certificate block in the store.</span></span>
-   <span data-ttu-id="1ad4a-119">Il puntatore "Next" nell'ultimo blocco certificate è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-119">The "next" pointer in the last certificate block is set to **NULL**.</span></span>
-   <span data-ttu-id="1ad4a-120">Il blocco di dati di un certificato contiene il contesto del certificato di sola lettura ed eventuali proprietà estese del certificato.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-120">The data block of a certificate contains the read-only certificate context and any extended properties of the certificate.</span></span>
-   <span data-ttu-id="1ad4a-121">Il blocco di dati di ogni certificato contiene un [*conteggio dei riferimenti*](../secgloss/r-gly.md) che tiene traccia del numero di puntatori al certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-121">The data block of each certificate contains a [*reference count*](../secgloss/r-gly.md) that keeps track of the number of pointers to the certificate that exist.</span></span>

<span data-ttu-id="1ad4a-122">I certificati in un [*archivio certificati*](../secgloss/c-gly.md) vengono in genere conservati in un tipo di archiviazione permanente, ad esempio un file su disco o il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-122">Certificates in a [*certificate store*](../secgloss/c-gly.md) are normally kept in some kind of permanent storage such as a disk file or the system registry.</span></span> <span data-ttu-id="1ad4a-123">Gli archivi certificati possono anche essere creati e aperti rigorosamente in memoria.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-123">Certificate stores can also be created and opened strictly in memory.</span></span> <span data-ttu-id="1ad4a-124">Un archivio di memoria fornisce l'archiviazione temporanea dei certificati per l'utilizzo di certificati che non devono essere conservati.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-124">A memory store provides temporary certificate storage for working with certificates that do not need to be kept.</span></span>

<span data-ttu-id="1ad4a-125">Percorsi di archiviazione aggiuntivi consentono di mantenere e cercare gli archivi in varie parti del registro di sistema di un computer locale o, con le autorizzazioni appropriate, nel registro di sistema in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-125">Additional store locations allow stores to be kept and searched in various parts of a local computer's registry or, with proper permissions set, in the registry on a remote computer.</span></span>

<span data-ttu-id="1ad4a-126">Ogni utente dispone di un archivio personale in cui sono archiviati i certificati dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-126">Each user has a personal My store where that user's certificates are stored.</span></span> <span data-ttu-id="1ad4a-127">L'archivio My può trovarsi in una qualsiasi delle numerose posizioni fisiche, incluso il registro di sistema in un computer locale o remoto, un file su disco, un database, un servizio directory, una [*Smart Card*](../secgloss/s-gly.md)o un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-127">The My store can be at any one of many physical locations, including the registry on a local or remote computer, a disk file, a database, directory service, a [*smart card*](../secgloss/s-gly.md), or another location.</span></span> <span data-ttu-id="1ad4a-128">Mentre un certificato può essere archiviato nell'archivio personale, questo archivio deve essere riservato ai certificati personali dell'utente, ovvero i certificati utilizzati per la firma e la decrittografia dei messaggi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-128">While any certificate can be stored in the My store, this store should be reserved for a user's personal certificates: those certificates used for signing and decrypting that user's messages.</span></span>

<span data-ttu-id="1ad4a-129">L'uso di certificati per l'autenticazione dipende dalla presenza di certificati emessi da un'autorità di certificazione attendibile.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-129">Using certificates for authentication depends on having certificates issued by some trusted certificate issuer.</span></span> <span data-ttu-id="1ad4a-130">I certificati per le autorità emittenti di certificati attendibili vengono in genere conservati nell'archivio radice, che è attualmente persistente in una sottochiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-130">Certificates for trusted certificate issuers are typically kept in the Root store, which is currently persisted to a registry subkey.</span></span> <span data-ttu-id="1ad4a-131">Nel contesto CryptoAPI l'archivio radice è protetto e le finestre di dialogo dell'interfaccia utente ricordano all'utente di inserire solo certificati attendibili nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-131">In the CryptoAPI context, the Root store is protected, and user interface dialog boxes remind the user to place only trusted certificates into that store.</span></span> <span data-ttu-id="1ad4a-132">Nelle situazioni di rete aziendale, i certificati possono essere inseriti (copiati) da un amministratore di sistema dal computer del controller di dominio agli archivi radice nei computer client.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-132">In enterprise network situations, certificates might be pushed (copied) by a system administrator from the domain controller computer to the Root stores on client computers.</span></span> <span data-ttu-id="1ad4a-133">Questo processo fornisce tutti i membri di un dominio con elenchi di attendibilità simili.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-133">This process provides all members of a domain with similar trust lists.</span></span>

<span data-ttu-id="1ad4a-134">Altri certificati possono essere archiviati nell'archivio di sistema dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) o negli archivi basati su file creati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-134">Other certificates can be stored in the [*certification authority*](../secgloss/c-gly.md) (CA) system store or in user-created, file-based stores.</span></span>

<span data-ttu-id="1ad4a-135">Per gli elenchi di funzioni per l'uso e la gestione di archivi certificati, vedere [funzioni dell'archivio certificati](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1ad4a-135">For lists of functions for using and maintaining certificate stores, see [Certificate Store Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="1ad4a-136">Per un esempio in cui vengono usate alcune di queste funzioni, vedere il [programma C di esempio: operazioni sull'archivio certificati](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1ad4a-136">For an example that uses some of these functions, see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ad4a-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ad4a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad4a-138">Gestione dello stato di un archivio certificati</span><span class="sxs-lookup"><span data-stu-id="1ad4a-138">Managing a Certificate Store State</span></span>](managing-a-certificate-store-state.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-139">Utilizzo dei certificati negli archivi certificati</span><span class="sxs-lookup"><span data-stu-id="1ad4a-139">Working with Certificates in Certificate Stores</span></span>](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-140">Collegamenti al certificato</span><span class="sxs-lookup"><span data-stu-id="1ad4a-140">Certificate Links</span></span>](certificate-links.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-141">Archivi della raccolta</span><span class="sxs-lookup"><span data-stu-id="1ad4a-141">Collection Stores</span></span>](collection-stores.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-142">Archivi logici e fisici</span><span class="sxs-lookup"><span data-stu-id="1ad4a-142">Logical and Physical Stores</span></span>](logical-and-physical-stores.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-143">Percorsi di archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="1ad4a-143">System Store Locations</span></span>](system-store-locations.md)
</dt> <dt>

[<span data-ttu-id="1ad4a-144">Migrazione dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="1ad4a-144">Certificate Store Migration</span></span>](certificate-store-migration.md)
</dt> </dl>

 

 
