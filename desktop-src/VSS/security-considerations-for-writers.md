---
description: L'infrastruttura VSS richiede che i processi writer siano in grado di funzionare sia come client COM sia come server.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considerazioni sulla sicurezza per i writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310670"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="dd546-103">Considerazioni sulla sicurezza per i writer</span><span class="sxs-lookup"><span data-stu-id="dd546-103">Security Considerations for Writers</span></span>

<span data-ttu-id="dd546-104">L'infrastruttura VSS richiede che i processi writer siano in grado di funzionare sia come client COM sia come server.</span><span class="sxs-lookup"><span data-stu-id="dd546-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="dd546-105">Quando funge da server, i writer VSS espongono le interfacce COM (ad esempio, i gestori eventi VSS, ad esempio [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) e ricevono chiamate com in ingresso da processi VSS (come i richiedenti e il servizio VSS) o chiamate RPC da processi esterni a VSS, in genere quando questi processi generano eventi VSS (ad esempio, quando un richiedente chiama [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span><span class="sxs-lookup"><span data-stu-id="dd546-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="dd546-106">Pertanto, un VSS writer deve gestire in modo sicuro quali client COM sono in grado di effettuare chiamate COM in ingresso al suo processo.</span><span class="sxs-lookup"><span data-stu-id="dd546-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="dd546-107">Analogamente, i writer VSS possono fungere anche da client COM, effettuando chiamate COM in uscita a callback forniti dall'infrastruttura VSS o chiamate RPC a processi esterni a VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="dd546-108">Questi callback forniti da un'applicazione di backup o dal servizio VSS consentono al writer di eseguire attività come l'aggiornamento del documento dei componenti di backup tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .</span><span class="sxs-lookup"><span data-stu-id="dd546-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="dd546-109">Pertanto, le impostazioni di sicurezza VSS devono consentire ai writer di eseguire chiamate COM in uscita in altri processi VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="dd546-110">Il meccanismo più semplice per la gestione dei problemi di sicurezza del writer riguarda la scelta corretta dell'account utente con cui viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd546-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="dd546-111">Un writer deve in genere essere eseguito con un utente membro del gruppo Administrators o del gruppo Backup Operators oppure deve essere eseguito come account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="dd546-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="dd546-112">Per impostazione predefinita, quando un writer funge da client COM, se non viene eseguito con questi account, qualsiasi chiamata COM che esegue viene rifiutata automaticamente con **E \_ AccessDenied** senza neanche dover ottenere l'implementazione del metodo com.</span><span class="sxs-lookup"><span data-stu-id="dd546-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="dd546-113">Disabilitazione della gestione delle eccezioni COM</span><span class="sxs-lookup"><span data-stu-id="dd546-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="dd546-114">Quando si sviluppa un writer, impostare il \_ \_ flag di opzioni globali di gestione delle eccezioni com COMGLB \_ per disabilitare la gestione delle eccezioni com.</span><span class="sxs-lookup"><span data-stu-id="dd546-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="dd546-115">È importante eseguire questa operazione perché la gestione delle eccezioni COM può mascherare gli errori irreversibili in un'applicazione VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="dd546-116">L'errore mascherato può lasciare il processo in uno stato instabile e imprevedibile, che può causare danneggiamenti e blocchi.</span><span class="sxs-lookup"><span data-stu-id="dd546-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="dd546-117">Per ulteriori informazioni su questo flag, vedere [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="dd546-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="dd546-118">Impostazione dell'autorizzazione per il controllo dell'accesso COM predefinito del writer</span><span class="sxs-lookup"><span data-stu-id="dd546-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="dd546-119">È necessario tenere presente che quando i processi fungono da server, ad esempio per gestire gli eventi VSS, devono consentire le chiamate in ingresso da altri partecipanti VSS, ad esempio i richiedenti o il servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="dd546-120">Tuttavia, per impostazione predefinita, un processo consentirà solo ai client COM che sono in esecuzione nella stessa sessione di accesso SID AUTONOMo o in esecuzione con l'account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="dd546-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="dd546-121">Questo è un potenziale problema perché queste impostazioni predefinite non sono sufficienti per supportare l'infrastruttura VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="dd546-122">Ad esempio, i richiedenti possono essere eseguiti come account utente "Backup Operator" che non si trova nella stessa sessione di accesso del processo di scrittura o di un account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="dd546-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="dd546-123">Per gestire questo tipo di problema, ogni processo server COM può esercitare un ulteriore controllo sul fatto che un client RPC o COM sia autorizzato a eseguire un metodo COM il server (in questo caso un writer) implementi utilizzando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare un'autorizzazione per il controllo dell'accesso COM predefinito a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="dd546-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="dd546-124">I writer possono eseguire in modo esplicito le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd546-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="dd546-125">Consente l'accesso a tutti i processi per chiamare il processo del writer.</span><span class="sxs-lookup"><span data-stu-id="dd546-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="dd546-126">Questa opzione può essere adeguata per molti writer e viene utilizzata da altri server COM. ad esempio, tutti i servizi Windows basati su SVCHOST utilizzano già questa opzione, così come tutti i servizi COM+ per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="dd546-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="dd546-127">Consentire a tutti i processi di eseguire chiamate COM in ingresso non è necessariamente un punto debole per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="dd546-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="dd546-128">Un writer che funge da server COM, come tutti gli altri server COM, mantiene sempre l'opzione di autorizzazione dei client su ogni metodo COM implementato nel processo.</span><span class="sxs-lookup"><span data-stu-id="dd546-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="dd546-129">Per consentire a tutti i processi l'accesso COM a un writer, è possibile passare un descrittore di sicurezza **null** come primo parametro di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="dd546-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="dd546-130">Si noti che **CoInitializeSecurity** deve essere chiamato al massimo una volta per l'intero processo.</span><span class="sxs-lookup"><span data-stu-id="dd546-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="dd546-131">Per ulteriori informazioni su **CoInitializeSecurity**, vedere la documentazione com.</span><span class="sxs-lookup"><span data-stu-id="dd546-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="dd546-132">Di seguito è riportato un esempio di codice che include una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span><span class="sxs-lookup"><span data-stu-id="dd546-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="dd546-133">Quando si imposta in modo esplicito la sicurezza a livello COM di un writer con [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd546-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="dd546-134">Impostare il livello di autenticazione su almeno **\_ \_ \_ \_ connessione a livello di autenticazione C RPC**.</span><span class="sxs-lookup"><span data-stu-id="dd546-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="dd546-135">Per una maggiore sicurezza, è consigliabile usare il **livello di autenticazione di RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="dd546-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="dd546-136">Impostare il livello di rappresentazione sull' **Identificazione del \_ \_ \_ livello \_ Imp C di RPC** , a meno che il processo writer non debba consentire la rappresentazione per chiamate RPC o com specifiche non correlate a VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="dd546-137">Consenti solo ai processi specificati l'accesso per chiamare il processo del writer.</span><span class="sxs-lookup"><span data-stu-id="dd546-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="dd546-138">Un server COM (ad esempio un writer) che chiama [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) con un descrittore di sicurezza non **null** può usare il descrittore per configurare se stesso in modo da accettare le chiamate in ingresso solo dagli utenti che appartengono a un set di account specifico.</span><span class="sxs-lookup"><span data-stu-id="dd546-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="dd546-139">Un writer deve garantire che i client COM in esecuzione in utenti validi siano autorizzati a chiamare il processo.</span><span class="sxs-lookup"><span data-stu-id="dd546-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="dd546-140">Un writer che specifica un descrittore di sicurezza nel primo parametro deve consentire agli utenti seguenti di eseguire chiamate in ingresso nel processo del richiedente:</span><span class="sxs-lookup"><span data-stu-id="dd546-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="dd546-141">Sistema locale</span><span class="sxs-lookup"><span data-stu-id="dd546-141">Local System</span></span>
    -   <span data-ttu-id="dd546-142">Membri del gruppo Administrators locale</span><span class="sxs-lookup"><span data-stu-id="dd546-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="dd546-143">Membri del gruppo Backup Operators locale</span><span class="sxs-lookup"><span data-stu-id="dd546-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="dd546-144">Account con cui è in esecuzione il writer</span><span class="sxs-lookup"><span data-stu-id="dd546-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="dd546-145">Controllo esplicito dell'accesso di un account utente a un writer</span><span class="sxs-lookup"><span data-stu-id="dd546-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="dd546-146">Ci sono casi in cui la limitazione dell'accesso a un writer ai processi in esecuzione come sistema locale o ai gruppi locali degli amministratori locali o degli operatori di backup locali può essere troppo restrittiva.</span><span class="sxs-lookup"><span data-stu-id="dd546-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="dd546-147">Ad esempio, un processo di scrittura (probabilmente un writer non di sistema di terze parti) potrebbe non essere in genere necessario per l'esecuzione con un account amministratore o operatore di backup.</span><span class="sxs-lookup"><span data-stu-id="dd546-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="dd546-148">Per motivi di sicurezza, è preferibile non innalzare di livello artificialmente i privilegi del processo per supportare VSS.</span><span class="sxs-lookup"><span data-stu-id="dd546-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="dd546-149">In questi casi, è necessario modificare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** per indicare a VSS che un utente specificato è sicuro per l'esecuzione di una VSS writer.</span><span class="sxs-lookup"><span data-stu-id="dd546-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="dd546-150">In questa chiave è necessario creare una sottochiave con lo stesso nome dell'account a cui viene concesso o negato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="dd546-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="dd546-151">Questa sottochiave deve essere impostata su uno dei valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dd546-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="dd546-152">Valore</span><span class="sxs-lookup"><span data-stu-id="dd546-152">Value</span></span> | <span data-ttu-id="dd546-153">Significato</span><span class="sxs-lookup"><span data-stu-id="dd546-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="dd546-154">0</span><span class="sxs-lookup"><span data-stu-id="dd546-154">0</span></span>     | <span data-ttu-id="dd546-155">Negare all'utente l'accesso al writer e al richiedente.</span><span class="sxs-lookup"><span data-stu-id="dd546-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="dd546-156">1</span><span class="sxs-lookup"><span data-stu-id="dd546-156">1</span></span>     | <span data-ttu-id="dd546-157">Concedere all'utente l'accesso al writer.</span><span class="sxs-lookup"><span data-stu-id="dd546-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="dd546-158">2</span><span class="sxs-lookup"><span data-stu-id="dd546-158">2</span></span>     | <span data-ttu-id="dd546-159">Concedere all'utente l'accesso al richiedente.</span><span class="sxs-lookup"><span data-stu-id="dd546-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="dd546-160">3</span><span class="sxs-lookup"><span data-stu-id="dd546-160">3</span></span>     | <span data-ttu-id="dd546-161">Concedere all'utente l'accesso al writer e al richiedente.</span><span class="sxs-lookup"><span data-stu-id="dd546-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="dd546-162">Nell'esempio seguente viene concesso l'accesso all'account "dominio \\ utente":</span><span class="sxs-lookup"><span data-stu-id="dd546-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="dd546-163">Questo meccanismo può essere usato anche per limitare in modo esplicito l'esecuzione di un VSS writer da un utente altrimenti consentito.</span><span class="sxs-lookup"><span data-stu-id="dd546-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="dd546-164">Nell'esempio seguente viene limitato l'accesso dall'account "ThatDomain \\ Administrator":</span><span class="sxs-lookup"><span data-stu-id="dd546-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="dd546-165">L' \\ amministratore di ThatDomain utente non sarà in grado di eseguire un VSS writer.</span><span class="sxs-lookup"><span data-stu-id="dd546-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
