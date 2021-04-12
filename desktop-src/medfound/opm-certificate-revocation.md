---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revoca del certificato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527889"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="21be5-103">Revoca del certificato OPM</span><span class="sxs-lookup"><span data-stu-id="21be5-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="21be5-104">Un certificato di output Protection Manager (OPM) può essere revocato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21be5-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="21be5-105">L'elenco dei certificati revocati viene archiviato in un elenco di revoche globale (GRL).</span><span class="sxs-lookup"><span data-stu-id="21be5-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="21be5-106">Il GRL ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="21be5-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21be5-107">Sezione</span><span class="sxs-lookup"><span data-stu-id="21be5-107">Section</span></span></th>
<th><span data-ttu-id="21be5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21be5-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21be5-109">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21be5-109">Header</span></span></td>
<td><span data-ttu-id="21be5-110">Struttura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="21be5-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21be5-111">Core</span><span class="sxs-lookup"><span data-stu-id="21be5-111">Core</span></span></td>
<td><span data-ttu-id="21be5-112">Contiene gli elenchi di revoche seguenti:</span><span class="sxs-lookup"><span data-stu-id="21be5-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="21be5-113">Revoche binarie del kernel</span><span class="sxs-lookup"><span data-stu-id="21be5-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="21be5-114">Revoche binarie in modalità utente</span><span class="sxs-lookup"><span data-stu-id="21be5-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="21be5-115">Revoche di certificati</span><span class="sxs-lookup"><span data-stu-id="21be5-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="21be5-116">Radici attendibili (riservato)</span><span class="sxs-lookup"><span data-stu-id="21be5-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="21be5-117">L'elenco di radici attendibili non viene attualmente utilizzato ed è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="21be5-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21be5-118">Voci estendibili</span><span class="sxs-lookup"><span data-stu-id="21be5-118">Extensible entries</span></span></td>
<td><span data-ttu-id="21be5-119">Contiene informazioni utilizzate da altri componenti.</span><span class="sxs-lookup"><span data-stu-id="21be5-119">Contains information used by other components.</span></span> <span data-ttu-id="21be5-120">Questa sezione non è pertinente per OPM.</span><span class="sxs-lookup"><span data-stu-id="21be5-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21be5-121">Rinnovi</span><span class="sxs-lookup"><span data-stu-id="21be5-121">Renewals:</span></span></td>
<td><span data-ttu-id="21be5-122">Contiene i GUID che definiscono gli identificatori di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="21be5-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="21be5-123">Questa sezione contiene gli identificatori per gli elenchi seguenti:</span><span class="sxs-lookup"><span data-stu-id="21be5-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="21be5-124">Revoche binarie del kernel</span><span class="sxs-lookup"><span data-stu-id="21be5-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="21be5-125">Revoche binarie in modalità utente</span><span class="sxs-lookup"><span data-stu-id="21be5-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="21be5-126">Revoche di certificati</span><span class="sxs-lookup"><span data-stu-id="21be5-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="21be5-127">Un'applicazione può usare questi identificatori per richiedere una versione rinnovata di un file binario revocato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="21be5-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21be5-128">Firma: sezione principale</span><span class="sxs-lookup"><span data-stu-id="21be5-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="21be5-129">Firma l'intestazione e le sezioni principali.</span><span class="sxs-lookup"><span data-stu-id="21be5-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21be5-130">Firma: sezione estendibile</span><span class="sxs-lookup"><span data-stu-id="21be5-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="21be5-131">Firma l'intestazione e le sezioni estendibili.</span><span class="sxs-lookup"><span data-stu-id="21be5-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="21be5-132">L'intestazione GRL è una struttura di [**\_ intestazione GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="21be5-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="21be5-133">Il membro **dwSequenceNumber** della struttura contiene il numero di versione di GRL.</span><span class="sxs-lookup"><span data-stu-id="21be5-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="21be5-134">Questo numero viene incrementato ogni volta che il GRL viene aggiornato e una nuova versione viene inserita nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21be5-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="21be5-135">I certificati OPM revocati sono elencati nell'elenco revoche di certificati della sezione principale.</span><span class="sxs-lookup"><span data-stu-id="21be5-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="21be5-136">Ogni voce principale in GRL è una matrice di 20 byte contenente l'hash SHA-1 della chiave pubblica del certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="21be5-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="21be5-137">Le sezioni della firma contengono le firme che possono essere usate per verificare che il GRL non sia stato alterato.</span><span class="sxs-lookup"><span data-stu-id="21be5-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="21be5-138">Ogni sezione della firma contiene la struttura della [**\_ firma AM MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="21be5-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="21be5-139">La prima firma firma l'intestazione più la sezione di base.</span><span class="sxs-lookup"><span data-stu-id="21be5-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="21be5-140">La seconda firma firma l'intestazione più la sezione estendibile; Questa firma non è pertinente per OPM.</span><span class="sxs-lookup"><span data-stu-id="21be5-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="21be5-141">Per assicurarsi che il GRL stesso non sia stato alterato, verificare la firma come segue:</span><span class="sxs-lookup"><span data-stu-id="21be5-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="21be5-142">Trovare l'inizio della struttura [**di \_ firma MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="21be5-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="21be5-143">Il percorso della struttura **di \_ firma MF** viene fornito nel membro **cbSignatureCoreOffset** della struttura dell' [**\_ intestazione GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="21be5-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="21be5-144">Il percorso viene specificato come offset in byte dall'inizio del GRL.</span><span class="sxs-lookup"><span data-stu-id="21be5-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="21be5-145">Analizzare la struttura di [**\_ firma MF**](mf-signature.md) come una \# firma PKCS 7 con una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="21be5-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="21be5-146">Verificare la catena di certificati fino a una radice attendibile.</span><span class="sxs-lookup"><span data-stu-id="21be5-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="21be5-147">Verificare che il certificato foglia includa il seguente identificatore di oggetto nell'EKU: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="21be5-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="21be5-148">Calcolare un hash dei byte che includono l'intestazione e le sezioni principali del GRL.</span><span class="sxs-lookup"><span data-stu-id="21be5-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="21be5-149">Verificare che l'hash corrisponda alla firma nel certificato foglia.</span><span class="sxs-lookup"><span data-stu-id="21be5-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21be5-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21be5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21be5-151">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="21be5-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="21be5-152">**\_intestazione GRL**</span><span class="sxs-lookup"><span data-stu-id="21be5-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="21be5-153">**\_firma MF**</span><span class="sxs-lookup"><span data-stu-id="21be5-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



