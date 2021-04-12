---
description: Un'infrastruttura a chiave pubblica (PKI) di Windows salva i certificati sul server che ospita l'autorità di certificazione (CA) e sul computer locale o sul dispositivo.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directory certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234170"
---
# <a name="certificate-directory"></a><span data-ttu-id="3f9bd-103">Directory certificati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-103">Certificate Directory</span></span>

<span data-ttu-id="3f9bd-104">Un'infrastruttura a chiave pubblica (PKI) di Windows salva i certificati sul server che ospita l'autorità di certificazione (CA) e sul computer locale o sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="3f9bd-105">L'archiviazione CA viene in genere definita database dei certificati e l'archiviazione locale è nota come archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="3f9bd-106">Database di certificati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-106">Certificate Database</span></span>

<span data-ttu-id="3f9bd-107">Quando si aggiungono servizi certificati in un server Windows e si configura una CA, viene creato un database di certificati.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="3f9bd-108">Per impostazione predefinita, il database è contenuto nella cartella *% systemroot%* \\ system32 \\ certlog e il nome è basato sul nome della CA con estensione edb.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="3f9bd-109">Il database può contenere:</span><span class="sxs-lookup"><span data-stu-id="3f9bd-109">The database can contain:</span></span>

-   <span data-ttu-id="3f9bd-110">Certificati emessi</span><span class="sxs-lookup"><span data-stu-id="3f9bd-110">Issued certificates</span></span>
-   <span data-ttu-id="3f9bd-111">Certificati revocati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-111">Revoked certificates</span></span>
-   <span data-ttu-id="3f9bd-112">Chiavi private archiviate</span><span class="sxs-lookup"><span data-stu-id="3f9bd-112">Archived private keys</span></span>
-   <span data-ttu-id="3f9bd-113">Richieste di certificati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-113">Certificate requests</span></span>

<span data-ttu-id="3f9bd-114">Non è possibile usare l'API di registrazione del certificato per modificare il database.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="3f9bd-115">Il processo di registrazione crea automaticamente le voci necessarie.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="3f9bd-116">Archivi certificati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-116">Certificate Stores</span></span>

<span data-ttu-id="3f9bd-117">Servizi certificati Microsoft copia i certificati emessi e le richieste in sospeso o rifiutate a computer e dispositivi locali.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="3f9bd-118">Il percorso di archiviazione è denominato archivio certificati ed è costituito dai seguenti archivi logici.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="3f9bd-119">Archivio logico</span><span class="sxs-lookup"><span data-stu-id="3f9bd-119">Logical store</span></span>                                         | <span data-ttu-id="3f9bd-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f9bd-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9bd-121">Personal</span><span class="sxs-lookup"><span data-stu-id="3f9bd-121">Personal</span></span><br/>                                   | <span data-ttu-id="3f9bd-122">Contiene i certificati associati a una chiave privata controllata dall'utente o dal computer.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="3f9bd-123">Autorità di certificazione radice disponibile nell'elenco locale</span><span class="sxs-lookup"><span data-stu-id="3f9bd-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="3f9bd-124">Contiene i certificati delle autorità di certificazione (CAs) implicitamente attendibili.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="3f9bd-125">Attendibilità per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="3f9bd-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="3f9bd-126">Contiene elenchi di certificati attendibili in genere utilizzati per considerare attendibili i certificati autofirmati di altre organizzazioni.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="3f9bd-127">Autorità di certificazione intermedie</span><span class="sxs-lookup"><span data-stu-id="3f9bd-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="3f9bd-128">Contiene i certificati emessi per le CA subordinate nella gerarchia di certificazione.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="3f9bd-129">Oggetto utente Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f9bd-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="3f9bd-130">Contiene il certificato dell'oggetto utente o i certificati pubblicati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="3f9bd-131">Autori attendibili</span><span class="sxs-lookup"><span data-stu-id="3f9bd-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="3f9bd-132">Contiene certificati provenienti da autorità di certificazione attendibili.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="3f9bd-133">Certificati non disponibili nell'elenco locale</span><span class="sxs-lookup"><span data-stu-id="3f9bd-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="3f9bd-134">Contiene i certificati che sono stati identificati in modo esplicito come non attendibili.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="3f9bd-135">CA principali di terze parti</span><span class="sxs-lookup"><span data-stu-id="3f9bd-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="3f9bd-136">Contiene certificati radice attendibili provenienti da autorità di certificazione esterne alla gerarchia di certificati interna.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="3f9bd-137">Persone attendibili</span><span class="sxs-lookup"><span data-stu-id="3f9bd-137">Trusted People</span></span><br/>                             | <span data-ttu-id="3f9bd-138">Contiene i certificati rilasciati a utenti o entità che sono stati esplicitamente attendibili.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="3f9bd-139">Altri utenti</span><span class="sxs-lookup"><span data-stu-id="3f9bd-139">Other People</span></span><br/>                               | <span data-ttu-id="3f9bd-140">Contiene i certificati rilasciati a utenti o entità considerati implicitamente attendibili.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="3f9bd-141">Richieste di registrazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="3f9bd-142">Contiene richieste di certificato in sospeso o rifiutate.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="3f9bd-143">Non è possibile usare l'API di registrazione certificati per specificare o recuperare le proprietà dell'archivio o copiare i certificati in archivi specifici.</span><span class="sxs-lookup"><span data-stu-id="3f9bd-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f9bd-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f9bd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f9bd-145">Elementi PKI</span><span class="sxs-lookup"><span data-stu-id="3f9bd-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




