---
description: Viene illustrata la procedura utilizzata per archiviare una chiave di sessione.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Archiviazione di una chiave di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312796"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="4bc97-103">Archiviazione di una chiave di sessione</span><span class="sxs-lookup"><span data-stu-id="4bc97-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="4bc97-104">In questa sezione si presuppone che gli utenti dispongano di un set di [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4bc97-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="4bc97-105">Le istruzioni e un esempio per la creazione di coppie di chiavi sono disponibili nel [programma C di esempio: creazione di un contenitore di chiavi e generazione di chiavi](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="4bc97-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="4bc97-106">**Per archiviare una chiave di sessione**</span><span class="sxs-lookup"><span data-stu-id="4bc97-106">**To store a session key**</span></span>

1.  <span data-ttu-id="4bc97-107">Creare un [*BLOB di chiavi*](../secgloss/k-gly.md) semplice usando la funzione [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="4bc97-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="4bc97-108">Questa operazione trasferirà la chiave della sessione dal CSP allo spazio di memoria di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4bc97-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="4bc97-109">Consente di specificare che verrà utilizzata una chiave pubblica di Exchange per firmare il BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="4bc97-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="4bc97-110">Archiviare il BLOB della chiave con segno su disco.</span><span class="sxs-lookup"><span data-stu-id="4bc97-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="4bc97-111">Si presuppone che tutti i dischi non siano sicuri.</span><span class="sxs-lookup"><span data-stu-id="4bc97-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="4bc97-112">Quando la chiave è necessaria, leggere il BLOB della chiave dal disco.</span><span class="sxs-lookup"><span data-stu-id="4bc97-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="4bc97-113">Importare di nuovo il BLOB della chiave nel CSP usando la funzione [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="4bc97-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="4bc97-114">Per un esempio di creazione di una [*chiave di sessione*](../secgloss/s-gly.md) e di esportazione della chiave in un BLOB di [*chiavi semplice*](../secgloss/s-gly.md) che può essere scritto in un file su disco, vedere [esempio C Program: exporting a Session Key](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="4bc97-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="4bc97-115">Questa procedura fornisce solo una sicurezza minima.</span><span class="sxs-lookup"><span data-stu-id="4bc97-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="4bc97-116">Se la chiave della sessione archiviata verrà utilizzata per crittografare i dati in un secondo momento, la procedura precedente non fornirà una sicurezza adeguata.</span><span class="sxs-lookup"><span data-stu-id="4bc97-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="4bc97-117">Per garantire una maggiore sicurezza, firmare il BLOB della chiave con una chiave privata di Exchange prima di archiviarlo su disco.</span><span class="sxs-lookup"><span data-stu-id="4bc97-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="4bc97-118">Quando il BLOB della chiave viene letto successivamente dal disco, la relativa firma può essere convalidata per garantire che il BLOB della chiave sia intatto.</span><span class="sxs-lookup"><span data-stu-id="4bc97-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="4bc97-119">Se il BLOB della chiave non è firmato, qualsiasi utente con accesso al disco o ad altri supporti in cui è archiviata la chiave può creare una nuova chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="4bc97-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="4bc97-120">La nuova chiave della sessione può essere crittografata con la [*chiave di scambio*](../secgloss/e-gly.md)della [*chiave pubblica*](../secgloss/p-gly.md) dell'utente originale e la nuova chiave può essere sostituita dall'originale.</span><span class="sxs-lookup"><span data-stu-id="4bc97-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="4bc97-121">Se l'utente ha usato inconsapevolmente la chiave della sessione sostituita per crittografare i file e i messaggi, la persona che ha creato il tasto sostitutivo potrebbe decrittografarli facilmente.</span><span class="sxs-lookup"><span data-stu-id="4bc97-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="4bc97-122">Le firme digitali sono descritte in dettaglio in [hash e firme digitali](hashes-and-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="4bc97-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
