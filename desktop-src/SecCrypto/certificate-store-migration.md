---
description: Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migrazione dell'archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058025"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="cab4e-103">Migrazione dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="cab4e-103">Certificate Store Migration</span></span>

<span data-ttu-id="cab4e-104">Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati.</span><span class="sxs-lookup"><span data-stu-id="cab4e-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="cab4e-105">Nella tabella seguente sono elencati gli archivi certificati per i quali viene eseguita la migrazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cab4e-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="cab4e-106">Per l'archivio impostazioni richiesta di certificato (ACRS) di sistema, viene eseguita la migrazione solo degli [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti).</span><span class="sxs-lookup"><span data-stu-id="cab4e-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="cab4e-107">Per tutti gli altri archivi elencati di seguito, vengono migrati solo i certificati.</span><span class="sxs-lookup"><span data-stu-id="cab4e-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cab4e-108">Sistema/utente</span><span class="sxs-lookup"><span data-stu-id="cab4e-108">System/user</span></span></th>
<th><span data-ttu-id="cab4e-109">Archivio</span><span class="sxs-lookup"><span data-stu-id="cab4e-109">Store</span></span></th>
<th><span data-ttu-id="cab4e-110">Posizione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cab4e-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cab4e-111">$ {ROWSPAN8} $System $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="cab4e-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="cab4e-112">RADICE</span><span class="sxs-lookup"><span data-stu-id="cab4e-112">ROOT</span></span></td>
<td><span data-ttu-id="cab4e-113"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-114">MY</span><span class="sxs-lookup"><span data-stu-id="cab4e-114">MY</span></span></td>
<td><span data-ttu-id="cab4e-115"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>My</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-116">RICHIESTA</span><span class="sxs-lookup"><span data-stu-id="cab4e-116">REQUEST</span></span></td>
<td><span data-ttu-id="cab4e-117"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Richiesta</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="cab4e-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="cab4e-119"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="cab4e-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="cab4e-121"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-122">Non consentita</span><span class="sxs-lookup"><span data-stu-id="cab4e-122">Disallowed</span></span></td>
<td><span data-ttu-id="cab4e-123"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>consentito</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-124">CA</span><span class="sxs-lookup"><span data-stu-id="cab4e-124">CA</span></span></td>
<td><span data-ttu-id="cab4e-125"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-126">ACRS</span><span class="sxs-lookup"><span data-stu-id="cab4e-126">ACRS</span></span></td>
<td><span data-ttu-id="cab4e-127"><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>Scopi consentiti</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="cab4e-128">Utente $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="cab4e-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="cab4e-129">RADICE</span><span class="sxs-lookup"><span data-stu-id="cab4e-129">ROOT</span></span></td>
<td><span data-ttu-id="cab4e-130"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-131">MY</span><span class="sxs-lookup"><span data-stu-id="cab4e-131">MY</span></span></td>
<td><span data-ttu-id="cab4e-132">file: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</span><span class="sxs-lookup"><span data-stu-id="cab4e-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-133">RICHIESTA</span><span class="sxs-lookup"><span data-stu-id="cab4e-133">REQUEST</span></span></td>
<td><span data-ttu-id="cab4e-134">file: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</span><span class="sxs-lookup"><span data-stu-id="cab4e-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="cab4e-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="cab4e-136"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="cab4e-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="cab4e-138"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="cab4e-139">Non consentita</span><span class="sxs-lookup"><span data-stu-id="cab4e-139">Disallowed</span></span></td>
<td><span data-ttu-id="cab4e-140"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>consentito</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="cab4e-141">CA</span><span class="sxs-lookup"><span data-stu-id="cab4e-141">CA</span></span></td>
<td><span data-ttu-id="cab4e-142"><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong></span><span class="sxs-lookup"><span data-stu-id="cab4e-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="cab4e-143">Per impostazione predefinita, non viene eseguita la migrazione di altri archivi certificati creati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cab4e-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="cab4e-144">Le applicazioni che creano i propri archivi sono responsabili della migrazione degli archivi creati.</span><span class="sxs-lookup"><span data-stu-id="cab4e-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="cab4e-145">Per creare archivi, è consigliabile definire una chiave del registro di sistema nelle impostazioni dell'applicazione e creare un archivio all'interno delle impostazioni del registro di sistema usando il provider **CERT \_ Store prove \_ \_ reg** Store.</span><span class="sxs-lookup"><span data-stu-id="cab4e-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="cab4e-146">Per ulteriori informazioni sulla migrazione delle impostazioni dell'applicazione, vedere l'argomento *How to create an Custom. xml file* nella Guida *using USMT 3,0* all' [utilità di migrazione stato utente 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span><span class="sxs-lookup"><span data-stu-id="cab4e-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="cab4e-147">Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="cab4e-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
