---
description: Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti servizio e gestione controllo servizi.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Sicurezza del servizio e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317679"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="cb8b1-103">Sicurezza del servizio e diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-103">Service Security and Access Rights</span></span>

<span data-ttu-id="cb8b1-104">Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti servizio e gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="cb8b1-105">Le sezioni seguenti forniscono informazioni dettagliate:</span><span class="sxs-lookup"><span data-stu-id="cb8b1-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="cb8b1-106">Diritti di accesso per Gestione controllo servizi</span><span class="sxs-lookup"><span data-stu-id="cb8b1-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="cb8b1-107">Diritti di accesso per un servizio</span><span class="sxs-lookup"><span data-stu-id="cb8b1-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="cb8b1-108">Diritti di accesso per Gestione controllo servizi</span><span class="sxs-lookup"><span data-stu-id="cb8b1-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="cb8b1-109">Di seguito sono riportati i diritti di accesso specifici per SCM.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="cb8b1-110">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-110">Access right</span></span>                                   | <span data-ttu-id="cb8b1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8b1-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8b1-112">**SC \_ GESTIONE \_ tutti gli \_ accessi** (0xF003F)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="cb8b1-113">Include **\_ i diritti standard \_ necessari**, oltre a tutti i diritti di accesso in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cb8b1-114">**SC \_ GESTIONE \_ creazione \_ servizio** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="cb8b1-115">Obbligatorio per chiamare la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per creare un oggetto servizio e aggiungerlo al database.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="cb8b1-116">**SC \_ GESTIONE \_ connessione** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="cb8b1-117">Obbligatorio per connettersi a gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cb8b1-118">**SC \_ GESTIONE \_ enumerazione \_ servizio** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="cb8b1-119">Obbligatorio per chiamare la funzione [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) o [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) per elencare i servizi presenti nel database.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="cb8b1-120">Obbligatorio per chiamare la funzione [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) per ricevere una notifica quando viene creato o eliminato un servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="cb8b1-121">**SC \_ \_Blocco gestione** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="cb8b1-122">Obbligatorio per chiamare la funzione [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) per acquisire un blocco sul database.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cb8b1-123">**SC \_ GESTIONE \_ modifica \_ \_ configurazione di avvio** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="cb8b1-124">Obbligatorio per chiamare la funzione [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb8b1-125">**SC \_ \_Stato di \_ blocco \_ della query di gestione** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="cb8b1-126">Obbligatorio per chiamare la funzione [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) per recuperare le informazioni sullo stato del blocco per il database.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="cb8b1-127">Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per SCM.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8b1-128">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-128">Access right</span></span></th>
<th><span data-ttu-id="cb8b1-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8b1-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb8b1-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="cb8b1-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="cb8b1-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="cb8b1-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="cb8b1-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8b1-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="cb8b1-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="cb8b1-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb8b1-144">Un processo con i diritti di accesso corretti può aprire un handle per SCM che può essere utilizzato nelle funzioni [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)e [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="cb8b1-145">Solo i processi con privilegi di amministratore sono in grado di aprire gli handle per SCM che possono essere usati dalle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="cb8b1-146">Il sistema crea il descrittore di sicurezza per SCM.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="cb8b1-147">Per ottenere o impostare il descrittore di sicurezza per SCM, utilizzare le funzioni [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) con un handle per l'oggetto SCManager.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="cb8b1-148">**Windows Server 2003 e Windows XP:** A differenza della maggior parte degli altri oggetti a protezione diretta, il descrittore di sicurezza per SCM non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="cb8b1-149">Questo comportamento è stato modificato a partire da Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cb8b1-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="cb8b1-150">Vengono concessi i seguenti diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8b1-151">Account</span><span class="sxs-lookup"><span data-stu-id="cb8b1-151">Account</span></span></th>
<th><span data-ttu-id="cb8b1-152">Diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb8b1-153">Utenti con autenticazione remota</span><span class="sxs-lookup"><span data-stu-id="cb8b1-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-155">Utenti autenticati locali (inclusi LocalService e NetworkService)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="cb8b1-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="cb8b1-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="cb8b1-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8b1-160">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="cb8b1-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="cb8b1-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="cb8b1-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="cb8b1-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="cb8b1-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-166">Administrators</span><span class="sxs-lookup"><span data-stu-id="cb8b1-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb8b1-168">Si noti che gli utenti remoti autenticati in rete ma non connessi in modo interattivo possono connettersi a SCM senza eseguire operazioni che richiedono altri diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="cb8b1-169">Per eseguire queste operazioni, è necessario che l'utente sia connesso in modo interattivo o che il servizio utilizzi uno degli account del servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="cb8b1-170">**Windows Server 2003 e Windows XP:** Agli utenti con autenticazione remota viene concesso il servizio **SC \_ Manager \_ Connect**, **SC \_ Manager \_ enumerate \_ Service**, **SC \_ Manager \_ query \_ lock \_ status** e Rights **\_ \_ Read** Rights Access Rights.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="cb8b1-171">Questi diritti di accesso sono limitati come descritto nella tabella precedente a partire da Windows Server 2003 con SP1</span><span class="sxs-lookup"><span data-stu-id="cb8b1-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="cb8b1-172">Quando un processo usa la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per aprire un handle per un database di servizi installati, può richiedere i diritti di accesso.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="cb8b1-173">Il sistema esegue un controllo di sicurezza rispetto al descrittore di sicurezza per SCM prima di concedere i diritti di accesso richiesti.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="cb8b1-174">Diritti di accesso per un servizio</span><span class="sxs-lookup"><span data-stu-id="cb8b1-174">Access Rights for a Service</span></span>

<span data-ttu-id="cb8b1-175">Di seguito sono riportati i diritti di accesso specifici per un servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="cb8b1-176">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-176">Access right</span></span>                                | <span data-ttu-id="cb8b1-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8b1-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8b1-178">**Servizio \_ di Tutti gli \_ accessi** (0xF01FF)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="cb8b1-179">Include **\_ i diritti standard \_ necessari** , oltre a tutti i diritti di accesso in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="cb8b1-180">**Servizio \_ di MODIFICA \_ configurazione** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="cb8b1-181">Obbligatorio per chiamare la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) per modificare la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="cb8b1-182">Poiché in questo modo il chiamante concede il diritto di modificare il file eseguibile eseguito dal sistema, deve essere concesso solo agli amministratori.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="cb8b1-183">**Servizio \_ di ENUMERA \_ dipendenti** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="cb8b1-184">Obbligatorio per chiamare la funzione [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) per enumerare tutti i servizi che dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="cb8b1-185">**Servizio \_ di INTERROGA** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="cb8b1-186">Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per chiedere al servizio di segnalare immediatamente lo stato.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cb8b1-187">**Servizio \_ di SOSPENDi \_ continua** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="cb8b1-188">Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per sospendere o continuare il servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cb8b1-189">**Servizio \_ di \_Configurazione query** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="cb8b1-190">Obbligatorio per chiamare le funzioni [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per eseguire una query sulla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="cb8b1-191">**Servizio \_ di \_Stato query** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="cb8b1-192">Obbligatorio per chiamare la funzione [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) per chiedere al gestore di controllo del servizio lo stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="cb8b1-193">Obbligatorio per chiamare la funzione [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) per ricevere una notifica quando viene modificato lo stato di un servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="cb8b1-194">**Servizio \_ di AVVIO** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="cb8b1-195">Obbligatorio per chiamare la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) per avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="cb8b1-196">**Servizio \_ di ARRESTA** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="cb8b1-197">Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per arrestare il servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cb8b1-198">**Servizio \_ di \_ \_ Controllo definito dall'utente**(0x0100)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="cb8b1-199">Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per specificare un codice di controllo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="cb8b1-200">Di seguito sono riportati i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) per un servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="cb8b1-201">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-201">Access right</span></span>                 | <span data-ttu-id="cb8b1-202">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8b1-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8b1-203">**ACCESSO \_ alla \_ sicurezza del sistema**</span><span class="sxs-lookup"><span data-stu-id="cb8b1-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="cb8b1-204">Obbligatorio per chiamare la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) o [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per accedere all'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="cb8b1-205">Il modo corretto per ottenere questo accesso consiste nell'abilitare il [**privilegio**](/windows/desktop/SecAuthZ/privileges) di **\_ sicurezza del \_ nome se** nel token di accesso corrente del chiamante, aprire l'handle per accedere alla **\_ \_ sicurezza del sistema** e quindi disabilitare il privilegio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="cb8b1-206">**Elimina**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="cb8b1-207">Obbligatorio per chiamare la funzione [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per eliminare il servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb8b1-208">**Leggi \_ CONTROLLO**  (0x20000)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="cb8b1-209">Obbligatorio per chiamare la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) per eseguire una query sul descrittore di sicurezza dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cb8b1-210">**Scrivi \_ Applicazione livello dati**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="cb8b1-211">Obbligatorio per chiamare la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per modificare il membro **DACL** del descrittore di sicurezza dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cb8b1-212">**Scrivi \_ PROPRIETARIO** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="cb8b1-213">Obbligatorio per chiamare la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per modificare i membri del **proprietario** e del **gruppo** del descrittore di sicurezza dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="cb8b1-214">Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8b1-215">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-215">Access right</span></span></th>
<th><span data-ttu-id="cb8b1-216">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb8b1-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb8b1-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="cb8b1-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="cb8b1-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="cb8b1-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="cb8b1-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="cb8b1-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8b1-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="cb8b1-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="cb8b1-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="cb8b1-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="cb8b1-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="cb8b1-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb8b1-232">Il gestore SCM Crea il descrittore di sicurezza di un oggetto servizio quando il servizio viene installato tramite la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="cb8b1-233">Il descrittore di sicurezza predefinito di un oggetto servizio concede il seguente accesso.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8b1-234">Account</span><span class="sxs-lookup"><span data-stu-id="cb8b1-234">Account</span></span></th>
<th><span data-ttu-id="cb8b1-235">Diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="cb8b1-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb8b1-236">Utenti con autenticazione remota</span><span class="sxs-lookup"><span data-stu-id="cb8b1-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="cb8b1-237">Non concessa per impostazione predefinita. <strong>Windows Server 2003 con SP1: SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="cb8b1-238"><strong>Windows Server 2003 e Windows XP:</strong> I diritti di accesso per gli utenti con autenticazione remota sono identici a quelli degli utenti autenticati locali.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-239">Utenti autenticati locali (inclusi LocalService e NetworkService)</span><span class="sxs-lookup"><span data-stu-id="cb8b1-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="cb8b1-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="cb8b1-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="cb8b1-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="cb8b1-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="cb8b1-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8b1-246">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="cb8b1-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="cb8b1-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="cb8b1-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="cb8b1-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="cb8b1-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="cb8b1-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="cb8b1-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="cb8b1-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="cb8b1-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8b1-256">Administrators</span><span class="sxs-lookup"><span data-stu-id="cb8b1-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="cb8b1-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="cb8b1-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="cb8b1-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="cb8b1-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="cb8b1-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="cb8b1-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb8b1-262">Per eseguire qualsiasi operazione, è necessario che l'utente sia connesso in modo interattivo o che il servizio utilizzi uno degli account del servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="cb8b1-263">Per ottenere o impostare il descrittore di sicurezza per un oggetto servizio, usare le funzioni [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="cb8b1-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="cb8b1-264">Per ulteriori informazioni, vedere [modifica dell'elenco DACL per un servizio](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="cb8b1-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="cb8b1-265">Quando un processo utilizza la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="cb8b1-266">La concessione di determinati diritti di accesso a utenti non attendibili, ad esempio la **\_ \_ configurazione delle modifiche dei servizi** o l' **\_ arresto del servizio**, può consentire loro di interferire con l'esecuzione del servizio e possibilmente consentire l'esecuzione di applicazioni con l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="cb8b1-267">Quando viene chiamata la [**funzione EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , se il chiamante non dispone del diritto di accesso **\_ \_ stato query del servizio** a un servizio, il servizio viene omesso automaticamente dall'elenco di servizi restituiti al client.</span><span class="sxs-lookup"><span data-stu-id="cb8b1-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

