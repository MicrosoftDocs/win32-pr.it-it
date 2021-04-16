---
description: L'infrastruttura VSS richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM sia come server.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considerazioni sulla sicurezza per i richiedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345011"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="7ba89-103">Considerazioni sulla sicurezza per i richiedenti</span><span class="sxs-lookup"><span data-stu-id="7ba89-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="7ba89-104">L'infrastruttura VSS richiede che i richiedenti VSS, ad esempio le applicazioni di backup, siano in grado di funzionare sia come client COM sia come server.</span><span class="sxs-lookup"><span data-stu-id="7ba89-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="7ba89-105">Quando funge da server, un richiedente espone un set di interfacce di callback COM che possono essere richiamate da processi esterni, ad esempio i writer o il servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="7ba89-106">Pertanto, i richiedenti devono gestire in modo sicuro quali client COM sono in grado di effettuare chiamate COM in ingresso al proprio processo.</span><span class="sxs-lookup"><span data-stu-id="7ba89-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="7ba89-107">Analogamente, i richiedenti possono fungere da client COM per le API COM fornite da un VSS writer o dal servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="7ba89-108">Le impostazioni di sicurezza specifiche del richiedente devono consentire le chiamate COM in uscita dal richiedente a questi altri processi.</span><span class="sxs-lookup"><span data-stu-id="7ba89-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="7ba89-109">Il meccanismo più semplice per la gestione dei problemi di sicurezza di un richiedente prevede una corretta selezione dell'account utente con cui viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ba89-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="7ba89-110">Un richiedente deve essere in genere eseguito con un utente membro del gruppo Administrators o del gruppo Backup Operators oppure viene eseguito come account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="7ba89-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="7ba89-111">Per impostazione predefinita, quando un richiedente funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM viene rifiutata automaticamente con **E \_ AccessDenied**, senza nemmeno ottenere l'implementazione del metodo com.</span><span class="sxs-lookup"><span data-stu-id="7ba89-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="7ba89-112">Disabilitazione della gestione delle eccezioni COM</span><span class="sxs-lookup"><span data-stu-id="7ba89-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="7ba89-113">Quando si sviluppa un richiedente, impostare il \_ \_ \_ flag di opzioni globali di gestione delle eccezioni com COMGLB per disabilitare la gestione delle eccezioni com.</span><span class="sxs-lookup"><span data-stu-id="7ba89-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="7ba89-114">È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="7ba89-115">L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi.</span><span class="sxs-lookup"><span data-stu-id="7ba89-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="7ba89-116">Per ulteriori informazioni su questo flag, vedere [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="7ba89-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="7ba89-117">Impostazione dell'autorizzazione per il controllo dell'accesso COM predefinito del richiedente</span><span class="sxs-lookup"><span data-stu-id="7ba89-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="7ba89-118">I richiedenti devono tenere presente che quando il processo funge da server (ad esempio, consentendo ai writer di modificare il documento dei componenti di backup), devono consentire le chiamate in ingresso da altri partecipanti VSS, ad esempio i writer o il servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="7ba89-119">Tuttavia, per impostazione predefinita, un processo di Windows consentirà solo i client COM in esecuzione nella stessa sessione di accesso (SID SELF) o in esecuzione con l'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="7ba89-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="7ba89-120">Questo è un potenziale problema perché queste impostazioni predefinite non sono adeguate all'infrastruttura VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="7ba89-121">Ad esempio, i writer potrebbero essere eseguiti come account utente "Backup Operator" che non si trova nella stessa sessione di accesso del processo del richiedente o di un account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="7ba89-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="7ba89-122">Per gestire questo tipo di problema, ogni processo server COM può esercitare un ulteriore controllo sul fatto che un client RPC o COM sia autorizzato a eseguire un metodo COM implementato dal server (in questo caso un richiedente) utilizzando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione di controllo di accesso COM predefinita a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="7ba89-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="7ba89-123">I richiedenti possono eseguire le operazioni seguenti in modo esplicito:</span><span class="sxs-lookup"><span data-stu-id="7ba89-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="7ba89-124">Consenti a tutti i processi l'accesso per chiamare il processo del richiedente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="7ba89-125">Questa opzione può essere adeguata per la maggior parte dei richiedenti e viene utilizzata da altri server COM. ad esempio, tutti i servizi Windows basati su SVCHOST utilizzano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ba89-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="7ba89-126">Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7ba89-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="7ba89-127">Un richiedente che funge da server COM, come tutti gli altri server COM, mantiene sempre l'opzione per autorizzare i client su ogni metodo COM implementato nel processo.</span><span class="sxs-lookup"><span data-stu-id="7ba89-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="7ba89-128">Si noti che i callback COM interni implementati da VSS sono protetti per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ba89-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="7ba89-129">Per consentire a tutti i processi l'accesso COM a un richiedente, è possibile passare un descrittore di sicurezza **null** come primo parametro di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7ba89-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7ba89-130">Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo.</span><span class="sxs-lookup"><span data-stu-id="7ba89-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="7ba89-131">Per ulteriori informazioni sulle chiamate **CoInitializeSecurity** , vedere la documentazione com o MSDN.</span><span class="sxs-lookup"><span data-stu-id="7ba89-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="7ba89-132">Nell'esempio di codice seguente viene illustrato come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 e windows Server 2012 e versioni successive, in modo da essere compatibile con VSS per le condivisioni file Remote (RVSS):</span><span class="sxs-lookup"><span data-stu-id="7ba89-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="7ba89-133">Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba89-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="7ba89-134">Impostare il livello di autenticazione almeno sull' **\_ \_ \_ \_ \_ integrità PKT del livello auth C RPC**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="7ba89-135">Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="7ba89-136">Impostare il livello di rappresentazione su **RPC \_ C \_ Imp \_ level \_ Impersonate**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="7ba89-137">Impostare le funzionalità di sicurezza mascheramento su **EOAC \_ static**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="7ba89-138">Per ulteriori informazioni sulla sicurezza del mascheramento, vedere [mascheramento](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="7ba89-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="7ba89-139">Nell'esempio di codice seguente viene illustrato come un richiedente deve chiamare [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 e windows Server 2008 R2 e versioni precedenti (oppure in Windows 8 e windows Server 2012 e versioni successive, se non è necessaria la compatibilità RVSS):</span><span class="sxs-lookup"><span data-stu-id="7ba89-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="7ba89-140">Quando si imposta in modo esplicito la sicurezza a livello COM di un richiedente con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba89-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="7ba89-141">Impostare il livello di autenticazione su almeno **\_ \_ \_ \_ connessione a livello di autenticazione C RPC**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="7ba89-142">Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="7ba89-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="7ba89-143">Impostare il livello di rappresentazione sull' **Identificazione del \_ \_ \_ livello \_ Imp C di RPC** , a meno che il processo del richiedente non debba consentire la rappresentazione per chiamate RPC o com specifiche che non sono correlate a VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="7ba89-144">Consenti solo ai processi specificati l'accesso per chiamare il processo del richiedente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="7ba89-145">Un server COM (ad esempio un richiedente) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **null** come primo parametro può usare il descrittore per configurare se stesso in modo da accettare le chiamate in ingresso solo dagli utenti che appartengono a un set di account specifico.</span><span class="sxs-lookup"><span data-stu-id="7ba89-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="7ba89-146">Un richiedente deve garantire che i client COM in esecuzione con utenti validi siano autorizzati a chiamare il processo.</span><span class="sxs-lookup"><span data-stu-id="7ba89-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="7ba89-147">Un richiedente che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo del richiedente:</span><span class="sxs-lookup"><span data-stu-id="7ba89-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="7ba89-148">Sistema locale</span><span class="sxs-lookup"><span data-stu-id="7ba89-148">Local System</span></span>
    -   <span data-ttu-id="7ba89-149">Servizio locale</span><span class="sxs-lookup"><span data-stu-id="7ba89-149">Local Service</span></span>

        <span data-ttu-id="7ba89-150">**Windows XP:** Questo valore non è supportato fino a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ba89-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="7ba89-151">Servizio di rete</span><span class="sxs-lookup"><span data-stu-id="7ba89-151">Network Service</span></span>

        <span data-ttu-id="7ba89-152">**Windows XP:** Questo valore non è supportato fino a Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ba89-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="7ba89-153">Membri del gruppo Administrators locale</span><span class="sxs-lookup"><span data-stu-id="7ba89-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="7ba89-154">Membri del gruppo Backup Operators locale</span><span class="sxs-lookup"><span data-stu-id="7ba89-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="7ba89-155">Utenti speciali specificati nel percorso del registro di sistema, con "1" come \_ valore DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7ba89-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="7ba89-156">Controllo esplicito dell'accesso degli account utente a un richiedente</span><span class="sxs-lookup"><span data-stu-id="7ba89-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="7ba89-157">Ci sono casi in cui la limitazione dell'accesso a un richiedente ai processi in esecuzione come sistema locale o ai gruppi Administrators locale o operatori di backup locale può essere troppo restrittiva.</span><span class="sxs-lookup"><span data-stu-id="7ba89-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="7ba89-158">Un processo del richiedente specificato, ad esempio, potrebbe non essere in genere necessario per l'esecuzione con un account amministratore o operatore di backup.</span><span class="sxs-lookup"><span data-stu-id="7ba89-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="7ba89-159">Per motivi di sicurezza, è preferibile non innalzare di livello artificialmente i privilegi dei processi per supportare VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="7ba89-160">In questi casi, è necessario modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** per indicare a VSS che un utente specificato è sicuro per l'esecuzione di un richiedente VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="7ba89-161">In questa chiave è necessario creare una sottochiave con lo stesso nome dell'account a cui viene concesso o negato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7ba89-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="7ba89-162">Questa sottochiave deve essere impostata su uno dei valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="7ba89-163">Valore</span><span class="sxs-lookup"><span data-stu-id="7ba89-163">Value</span></span> | <span data-ttu-id="7ba89-164">Significato</span><span class="sxs-lookup"><span data-stu-id="7ba89-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="7ba89-165">0</span><span class="sxs-lookup"><span data-stu-id="7ba89-165">0</span></span>     | <span data-ttu-id="7ba89-166">Negare all'utente l'accesso al writer e al richiedente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="7ba89-167">1</span><span class="sxs-lookup"><span data-stu-id="7ba89-167">1</span></span>     | <span data-ttu-id="7ba89-168">Concedere all'utente l'accesso al writer.</span><span class="sxs-lookup"><span data-stu-id="7ba89-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="7ba89-169">2</span><span class="sxs-lookup"><span data-stu-id="7ba89-169">2</span></span>     | <span data-ttu-id="7ba89-170">Concedere all'utente l'accesso al richiedente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="7ba89-171">3</span><span class="sxs-lookup"><span data-stu-id="7ba89-171">3</span></span>     | <span data-ttu-id="7ba89-172">Concedere all'utente l'accesso al writer e al richiedente.</span><span class="sxs-lookup"><span data-stu-id="7ba89-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="7ba89-173">Nell'esempio seguente viene concesso l'accesso all'account "dominio \\ utente":</span><span class="sxs-lookup"><span data-stu-id="7ba89-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="7ba89-174">Questo meccanismo può essere usato anche per limitare in modo esplicito l'esecuzione di un richiedente VSS a un utente altrimenti consentito.</span><span class="sxs-lookup"><span data-stu-id="7ba89-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="7ba89-175">Nell'esempio seguente viene limitato l'accesso dall'account "ThatDomain \\ Administrator":</span><span class="sxs-lookup"><span data-stu-id="7ba89-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="7ba89-176">L' \\ amministratore di ThatDomain utente non sarà in grado di eseguire un richiedente VSS.</span><span class="sxs-lookup"><span data-stu-id="7ba89-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="7ba89-177">Esecuzione di un backup di file dello stato del sistema</span><span class="sxs-lookup"><span data-stu-id="7ba89-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="7ba89-178">Se un richiedente esegue il backup dello stato del sistema eseguendo il backup di singoli file anziché usare un'immagine del volume per il backup, deve chiamare le funzioni [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) per enumerare i collegamenti reali nei file che si trovano nelle directory seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ba89-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="7ba89-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="7ba89-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="7ba89-180">Windows \\ WINSXS</span><span class="sxs-lookup"><span data-stu-id="7ba89-180">Windows\\WINSXS</span></span>\\

<span data-ttu-id="7ba89-181">È possibile accedere a tali directory solo da membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="7ba89-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="7ba89-182">Per questo motivo, tale richiedente deve essere eseguito con l'account di sistema o con un account utente membro del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="7ba89-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="7ba89-183">**Windows XP e Windows Server 2003:** Le funzioni [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) non sono supportate fino a Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7ba89-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
