---
description: Un archivio di sistema è una raccolta costituita da uno o più archivi di pari livello fisici.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Percorsi di archivio di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967619"
---
# <a name="system-store-locations"></a><span data-ttu-id="9a68a-103">Percorsi di archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-103">System Store Locations</span></span>

<span data-ttu-id="9a68a-104">Un archivio di sistema è una raccolta costituita da uno o più archivi di pari livello fisici.</span><span class="sxs-lookup"><span data-stu-id="9a68a-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="9a68a-105">Per ogni archivio di sistema sono presenti archivi di pari livello fisici predefiniti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="9a68a-106">Dopo l'apertura di un archivio di sistema come MY at CERT \_ System \_ Store \_ Current \_ User, il provider dell'archivio chiama [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) per aprire tutti gli archivi fisici nella raccolta di archivi di sistema.</span><span class="sxs-lookup"><span data-stu-id="9a68a-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="9a68a-107">Nel processo aperto ognuno di questi archivi fisici viene aggiunto alla raccolta di archivi di sistema tramite [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span><span class="sxs-lookup"><span data-stu-id="9a68a-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="9a68a-108">Tutti i certificati in tali archivi fisici sono disponibili tramite la raccolta di archivi di sistema logici.</span><span class="sxs-lookup"><span data-stu-id="9a68a-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="9a68a-109">Per ogni percorso di archivio di sistema, gli archivi di sistemi predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="9a68a-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="9a68a-110">MY</span><span class="sxs-lookup"><span data-stu-id="9a68a-110">MY</span></span>
-   <span data-ttu-id="9a68a-111">Radice</span><span class="sxs-lookup"><span data-stu-id="9a68a-111">Root</span></span>
-   <span data-ttu-id="9a68a-112">Trust</span><span class="sxs-lookup"><span data-stu-id="9a68a-112">Trust</span></span>
-   <span data-ttu-id="9a68a-113">CA</span><span class="sxs-lookup"><span data-stu-id="9a68a-113">CA</span></span>

<span data-ttu-id="9a68a-114">Nell' \_ \_ \_ utente corrente dell'archivio CERT System \_ è presente anche un archivio UserDS predefinito.</span><span class="sxs-lookup"><span data-stu-id="9a68a-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="9a68a-115">Un archivio di smart card è pianificato per questo percorso.</span><span class="sxs-lookup"><span data-stu-id="9a68a-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="9a68a-116">Ecco gli archivi di sistema seguiti da ulteriori osservazioni:</span><span class="sxs-lookup"><span data-stu-id="9a68a-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="9a68a-117">\_ \_ \_ utente corrente archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="9a68a-118">\_ \_ \_ computer locale archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="9a68a-119">\_ \_ \_ servizio corrente archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="9a68a-120">\_servizi di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="9a68a-121">\_utenti di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="9a68a-122">\_criteri di \_ \_ gruppo dell'utente corrente \_ del \_ sistema CERT</span><span class="sxs-lookup"><span data-stu-id="9a68a-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="9a68a-123">\_criteri di \_ \_ gruppo del computer locale \_ di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="9a68a-124">\_Archivio di sistema CERT \_ \_ \_ computer locale \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a68a-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="9a68a-125">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="9a68a-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="9a68a-126">\_ \_ \_ utente corrente archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="9a68a-127">\_ \_ \_ \_ Gli archivi di sistema degli utenti correnti del sistema di certificati si trovano nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="9a68a-128">Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-129">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-129">System store</span></span> | <span data-ttu-id="9a68a-130">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="9a68a-131">MY</span><span class="sxs-lookup"><span data-stu-id="9a68a-131">MY</span></span>           | <span data-ttu-id="9a68a-132">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-132">.Default</span></span>                                                 |
| <span data-ttu-id="9a68a-133">Radice</span><span class="sxs-lookup"><span data-stu-id="9a68a-133">Root</span></span>         | <span data-ttu-id="9a68a-134">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="9a68a-135">. Smart Card</span><span class="sxs-lookup"><span data-stu-id="9a68a-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="9a68a-136">Trust</span><span class="sxs-lookup"><span data-stu-id="9a68a-136">Trust</span></span>        | <span data-ttu-id="9a68a-137">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="9a68a-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="9a68a-138">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-139">CA</span><span class="sxs-lookup"><span data-stu-id="9a68a-139">CA</span></span>           | <span data-ttu-id="9a68a-140">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="9a68a-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="9a68a-141">. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-142">UserDS</span><span class="sxs-lookup"><span data-stu-id="9a68a-142">UserDS</span></span>       | <span data-ttu-id="9a68a-143">. UserCertificate</span><span class="sxs-lookup"><span data-stu-id="9a68a-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="9a68a-144">\_ \_ \_ computer locale archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="9a68a-145">\_ \_ \_ \_ Gli archivi di sistema del computer locale dell'archivio del sistema CERT si trovano nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="9a68a-146">Gli archivi fisici predefiniti sono associati a tali archivi di sistema, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="9a68a-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-147">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-147">System store</span></span> | <span data-ttu-id="9a68a-148">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a68a-149">MY</span><span class="sxs-lookup"><span data-stu-id="9a68a-149">MY</span></span>           | <span data-ttu-id="9a68a-150">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="9a68a-151">Radice</span><span class="sxs-lookup"><span data-stu-id="9a68a-151">Root</span></span>         | <span data-ttu-id="9a68a-152">. Default. AuthRoot</span><span class="sxs-lookup"><span data-stu-id="9a68a-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="9a68a-153">. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="9a68a-153">.GroupPolicy</span></span><br/> <span data-ttu-id="9a68a-154">. Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a68a-154">.Enterprise</span></span><br/> <span data-ttu-id="9a68a-155">. Smart Card</span><span class="sxs-lookup"><span data-stu-id="9a68a-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="9a68a-156">Trust</span><span class="sxs-lookup"><span data-stu-id="9a68a-156">Trust</span></span>        | <span data-ttu-id="9a68a-157">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="9a68a-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="9a68a-158">. Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a68a-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="9a68a-159">CA</span><span class="sxs-lookup"><span data-stu-id="9a68a-159">CA</span></span>           | <span data-ttu-id="9a68a-160">. Default. GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="9a68a-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="9a68a-161">. Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a68a-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="9a68a-162">\_ \_ \_ servizio corrente archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="9a68a-163">\_ \_ \_ \_ Gli archivi del sistema del servizio di archiviazione del sistema CERT correnti si trovano nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="9a68a-164">Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-165">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-165">System store</span></span> | <span data-ttu-id="9a68a-166">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="9a68a-167">MY</span><span class="sxs-lookup"><span data-stu-id="9a68a-167">MY</span></span>           | <span data-ttu-id="9a68a-168">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-168">.Default</span></span>                         |
| <span data-ttu-id="9a68a-169">Radice</span><span class="sxs-lookup"><span data-stu-id="9a68a-169">Root</span></span>         | <span data-ttu-id="9a68a-170">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-171">Trust</span><span class="sxs-lookup"><span data-stu-id="9a68a-171">Trust</span></span>        | <span data-ttu-id="9a68a-172">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-173">CA</span><span class="sxs-lookup"><span data-stu-id="9a68a-173">CA</span></span>           | <span data-ttu-id="9a68a-174">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="9a68a-175">\_servizi di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="9a68a-176">\_ \_ \_ Gli archivi di sistema di CERT System Store Services si trovano nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="9a68a-177">Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-178">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-178">System store</span></span>       | <span data-ttu-id="9a68a-179">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="9a68a-180">ServiceName \\ My</span><span class="sxs-lookup"><span data-stu-id="9a68a-180">ServiceName\\MY</span></span>    | <span data-ttu-id="9a68a-181">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-181">.Default</span></span>                         |
| <span data-ttu-id="9a68a-182">Radice ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="9a68a-182">ServiceName\\Root</span></span>  | <span data-ttu-id="9a68a-183">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-184">Trust di ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="9a68a-184">ServiceName\\Trust</span></span> | <span data-ttu-id="9a68a-185">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-186">CA ServiceName \\</span><span class="sxs-lookup"><span data-stu-id="9a68a-186">ServiceName\\CA</span></span>    | <span data-ttu-id="9a68a-187">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="9a68a-188">\_utenti di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="9a68a-189">\_ \_ \_ Gli archivi di sistema CERT System Store Users si trovano nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="9a68a-190">Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-191">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-191">System store</span></span>  | <span data-ttu-id="9a68a-192">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="9a68a-193">ID \\ utente</span><span class="sxs-lookup"><span data-stu-id="9a68a-193">userid\\MY</span></span>    | <span data-ttu-id="9a68a-194">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-195">\\radice UserID</span><span class="sxs-lookup"><span data-stu-id="9a68a-195">userid\\Root</span></span>  | <span data-ttu-id="9a68a-196">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-197">\\attendibilità UserID</span><span class="sxs-lookup"><span data-stu-id="9a68a-197">userid\\Trust</span></span> | <span data-ttu-id="9a68a-198">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="9a68a-199">\\CA UserID</span><span class="sxs-lookup"><span data-stu-id="9a68a-199">userid\\CA</span></span>    | <span data-ttu-id="9a68a-200">. Default. LocalMachine</span><span class="sxs-lookup"><span data-stu-id="9a68a-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="9a68a-201">\_criteri di \_ \_ gruppo dell'utente corrente \_ del \_ sistema CERT</span><span class="sxs-lookup"><span data-stu-id="9a68a-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="9a68a-202">\_ \_ \_ \_ \_ Gli archivi di sistema di criteri di gruppo dell'utente corrente del sistema CERT sono nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="9a68a-203">\_criteri di \_ \_ gruppo del computer locale \_ di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="9a68a-204">\_ \_ \_ \_ \_ Gli archivi di sistema di criteri di gruppo del computer locale di sistema CERT sono nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="9a68a-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="9a68a-205">\_Archivio di sistema CERT \_ \_ \_ computer locale \_ Enterprise</span><span class="sxs-lookup"><span data-stu-id="9a68a-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="9a68a-206">Il \_ \_ computer locale dell'archivio del sistema CERT \_ contiene i \_ \_ certificati condivisi tra domini nell'azienda e scaricati dalla directory globale dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a68a-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="9a68a-207">Per sincronizzare l'archivio aziendale del client, viene eseguito il polling della directory aziendale ogni otto ore e i certificati vengono scaricati automaticamente in background.</span><span class="sxs-lookup"><span data-stu-id="9a68a-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="9a68a-208">Gli archivi fisici predefiniti associati a questi archivi di sistema sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a68a-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="9a68a-209">Archivio di sistema</span><span class="sxs-lookup"><span data-stu-id="9a68a-209">System store</span></span> | <span data-ttu-id="9a68a-210">Archivio fisico</span><span class="sxs-lookup"><span data-stu-id="9a68a-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="9a68a-211">MY</span><span class="sxs-lookup"><span data-stu-id="9a68a-211">MY</span></span>           | <span data-ttu-id="9a68a-212">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-212">.Default</span></span>       |
| <span data-ttu-id="9a68a-213">Radice</span><span class="sxs-lookup"><span data-stu-id="9a68a-213">Root</span></span>         | <span data-ttu-id="9a68a-214">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-214">.Default</span></span>       |
| <span data-ttu-id="9a68a-215">Trust</span><span class="sxs-lookup"><span data-stu-id="9a68a-215">Trust</span></span>        | <span data-ttu-id="9a68a-216">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-216">.Default</span></span>       |
| <span data-ttu-id="9a68a-217">CA</span><span class="sxs-lookup"><span data-stu-id="9a68a-217">CA</span></span>           | <span data-ttu-id="9a68a-218">. Predefinita</span><span class="sxs-lookup"><span data-stu-id="9a68a-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="9a68a-219">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a68a-219">Remarks</span></span>

<span data-ttu-id="9a68a-220">Gli archivi fisici aggiuntivi possono essere associati a un archivio di sistema tramite [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="9a68a-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="9a68a-221">Gli \_ archivi CERT System \_ Store \_ Service e CERT \_ System \_ Store \_ Users vengono aperti anteponendo il nome dell'archivio nella stringa passata a *pvPara* con il nome del servizio o dell'utente, ad esempio *ServiceName* \\ **trust** o **. Predefinito** \\ **My**.</span><span class="sxs-lookup"><span data-stu-id="9a68a-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="9a68a-222">Il percorso CERT System \_ \_ Store \_ Services o CERT \_ System \_ Store \_ Users può aprire lo stesso archivio in cert \_ System \_ Current \_ Service o CERT \_ System \_ Store \_ utente corrente \_ usando l'ID di [*sicurezza*](../secgloss/s-gly.md) testuale (SID) del servizio o dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="9a68a-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="9a68a-223">Gli archivi nei criteri di \_ \_ \_ gruppo dell'utente dell'archivio di sistema CERT \_ \_ e \_ dei criteri di gruppo del computer \_ locale del sistema CERT \_ \_ \_ in un'impostazione di rete vengono scaricati nel computer client dal modello di criteri di gruppo (GPT) durante l'avvio del computer o l'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9a68a-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="9a68a-224">Questi archivi possono essere aggiornati nel computer client dopo l'avvio o l'accesso quando il GPT viene modificato nel server di dominio da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="9a68a-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="9a68a-225">La funzione [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) consente a un'applicazione di ricevere una notifica quando vengono modificati i negozi in una di queste posizioni.</span><span class="sxs-lookup"><span data-stu-id="9a68a-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="9a68a-226">È possibile aprire in remoto i percorsi di archivio di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a68a-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="9a68a-227">\_ \_ \_ computer locale archivio certificati di sistema \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="9a68a-228">\_criteri di \_ \_ gruppo del \_ computer \_ locale \_ dell'archivio di sistema CERT</span><span class="sxs-lookup"><span data-stu-id="9a68a-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="9a68a-229">\_servizi di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="9a68a-230">\_utenti di \_ Archivio di sistema CERT \_</span><span class="sxs-lookup"><span data-stu-id="9a68a-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="9a68a-231">I percorsi dell'archivio di sistema vengono aperti in modalità remota anteponendo il nome dell'archivio nella stringa passata a *pvPara* con il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="9a68a-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="9a68a-232">Esempi di nomi di archivio di sistema remoto sono:</span><span class="sxs-lookup"><span data-stu-id="9a68a-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="9a68a-233">*Nomecomputer* \\ **CA**</span><span class="sxs-lookup"><span data-stu-id="9a68a-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="9a68a-234">\\\\*Nomecomputer* \\ **CA**</span><span class="sxs-lookup"><span data-stu-id="9a68a-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="9a68a-235">*Nomecomputer* \\ *ServiceName* \\ **Attendibilità**</span><span class="sxs-lookup"><span data-stu-id="9a68a-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="9a68a-236">\\\\*Nomecomputer* \\ *ServiceName* \\ **Attendibilità**</span><span class="sxs-lookup"><span data-stu-id="9a68a-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
