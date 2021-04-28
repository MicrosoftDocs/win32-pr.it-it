---
description: Revoca del certificato OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revoca del certificato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092729"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="d427e-103">Revoca del certificato OPM</span><span class="sxs-lookup"><span data-stu-id="d427e-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="d427e-104">Un certificato OPM (Output Protection Manager) può essere revocato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d427e-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="d427e-105">L'elenco di certificati revocati viene archiviato in un elenco di revoche globale.</span><span class="sxs-lookup"><span data-stu-id="d427e-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="d427e-106">Il formato grl è il seguente:</span><span class="sxs-lookup"><span data-stu-id="d427e-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d427e-107">Sezione</span><span class="sxs-lookup"><span data-stu-id="d427e-107">Section</span></span></th>
<th><span data-ttu-id="d427e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d427e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d427e-109">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d427e-109">Header</span></span></td>
<td><span data-ttu-id="d427e-110">Struttura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> corrente.</span><span class="sxs-lookup"><span data-stu-id="d427e-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d427e-111">Core</span><span class="sxs-lookup"><span data-stu-id="d427e-111">Core</span></span></td>
<td><span data-ttu-id="d427e-112">Contiene gli elenchi di revoche seguenti:</span><span class="sxs-lookup"><span data-stu-id="d427e-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="d427e-113">Revoche binarie del kernel</span><span class="sxs-lookup"><span data-stu-id="d427e-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="d427e-114">Revoche binarie in modalità utente</span><span class="sxs-lookup"><span data-stu-id="d427e-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="d427e-115">Revoche di certificati</span><span class="sxs-lookup"><span data-stu-id="d427e-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="d427e-116">Radici attendibili (riservate)</span><span class="sxs-lookup"><span data-stu-id="d427e-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="d427e-117">L'elenco di radici attendibili non viene attualmente usato ed è riservato per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d427e-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d427e-118">Voci estendibili</span><span class="sxs-lookup"><span data-stu-id="d427e-118">Extensible entries</span></span></td>
<td><span data-ttu-id="d427e-119">Contiene informazioni utilizzate da altri componenti.</span><span class="sxs-lookup"><span data-stu-id="d427e-119">Contains information used by other components.</span></span> <span data-ttu-id="d427e-120">Questa sezione non è pertinente per OPM.</span><span class="sxs-lookup"><span data-stu-id="d427e-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d427e-121">Rinnovi:</span><span class="sxs-lookup"><span data-stu-id="d427e-121">Renewals:</span></span></td>
<td><span data-ttu-id="d427e-122">Contiene GUID che definiscono Windows Update identificatori.</span><span class="sxs-lookup"><span data-stu-id="d427e-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="d427e-123">Questa sezione contiene gli identificatori per gli elenchi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d427e-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="d427e-124">Revoche binarie del kernel</span><span class="sxs-lookup"><span data-stu-id="d427e-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="d427e-125">Revoche binarie in modalità utente</span><span class="sxs-lookup"><span data-stu-id="d427e-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="d427e-126">Revoche di certificati</span><span class="sxs-lookup"><span data-stu-id="d427e-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="d427e-127">Un'applicazione può usare questi identificatori per richiedere una versione rinnovata di un file binario revocato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="d427e-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d427e-128">Firma: sezione Core</span><span class="sxs-lookup"><span data-stu-id="d427e-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="d427e-129">Firma l'intestazione e le sezioni principali.</span><span class="sxs-lookup"><span data-stu-id="d427e-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d427e-130">Firma: sezione Estendibile</span><span class="sxs-lookup"><span data-stu-id="d427e-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="d427e-131">Firma l'intestazione e le sezioni estensibili.</span><span class="sxs-lookup"><span data-stu-id="d427e-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d427e-132">L'intestazione GRL è una [**struttura GRL \_ HEADER.**](grl-header.md)</span><span class="sxs-lookup"><span data-stu-id="d427e-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="d427e-133">Il **membro dwSequenceNumber** della struttura contiene il numero di versione GRL.</span><span class="sxs-lookup"><span data-stu-id="d427e-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="d427e-134">Questo numero viene incrementato ogni volta che il grl viene aggiornato e una nuova versione inserita nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d427e-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="d427e-135">I certificati OPM revocati sono elencati nell'elenco delle revoche di certificati della sezione Core.</span><span class="sxs-lookup"><span data-stu-id="d427e-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="d427e-136">Ogni voce core nella grl è una matrice di 20 byte che contiene l'hash SHA-1 della chiave pubblica del certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="d427e-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="d427e-137">Le sezioni Firma contengono firme che possono essere usate per verificare che l'grl non sia stato manomesso.</span><span class="sxs-lookup"><span data-stu-id="d427e-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="d427e-138">Ogni sezione Signature contiene la [**struttura MF \_ SIGNATURE.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="d427e-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="d427e-139">La prima firma firma l'intestazione più la sezione Core.</span><span class="sxs-lookup"><span data-stu-id="d427e-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="d427e-140">La seconda firma firma l'intestazione e la sezione Estendibile. questa firma non è pertinente per OPM.</span><span class="sxs-lookup"><span data-stu-id="d427e-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="d427e-141">Per assicurarsi che l'grl non sia stato manomesso, verificare la firma come segue:</span><span class="sxs-lookup"><span data-stu-id="d427e-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="d427e-142">Trovare l'inizio della [**struttura MF \_ SIGNATURE.**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="d427e-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="d427e-143">La posizione della **struttura MF \_ SIGNATURE** è specificata nel membro **cbSignatureCoreOffset** della [**struttura GRL \_ HEADER.**](grl-header.md)</span><span class="sxs-lookup"><span data-stu-id="d427e-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="d427e-144">La posizione viene specificata come offset in byte dall'inizio dell'oggetto GRL.</span><span class="sxs-lookup"><span data-stu-id="d427e-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="d427e-145">Analizzare la [**struttura MF \_ SIGNATURE**](mf-signature.md) come firma PKCS \# 7 con una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="d427e-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="d427e-146">Verificare la catena di certificati fino a una radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="d427e-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="d427e-147">Verificare che il certificato foglia abbia l'identificatore di oggetto seguente nell'EKU: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="d427e-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="d427e-148">Calcolare un hash dei byte che includono l'intestazione e le sezioni principali dell'oggetto GRL.</span><span class="sxs-lookup"><span data-stu-id="d427e-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="d427e-149">Verificare che l'hash corrisponda alla firma nel certificato foglia.</span><span class="sxs-lookup"><span data-stu-id="d427e-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d427e-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d427e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d427e-151">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="d427e-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="d427e-152">**INTESTAZIONE \_ GRL**</span><span class="sxs-lookup"><span data-stu-id="d427e-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="d427e-153">**FIRMA \_ MF**</span><span class="sxs-lookup"><span data-stu-id="d427e-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



