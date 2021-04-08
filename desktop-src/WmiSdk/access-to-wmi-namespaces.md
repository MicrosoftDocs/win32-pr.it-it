---
description: WMI utilizza un descrittore di sicurezza standard di Windows per controllare l'accesso agli spazi dei nomi WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Accesso agli spazi dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968373"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="6665f-103">Accesso agli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="6665f-104">WMI utilizza un *descrittore di sicurezza* standard di Windows per controllare l'accesso agli spazi dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="6665f-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="6665f-105">Quando ci si connette a WMI, tramite il moniker "winmgmts" WMI o una chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) o [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), si esegue la connessione a uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="6665f-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="6665f-106">Le informazioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="6665f-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="6665f-107">Sicurezza dello spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="6665f-108">Controllo dello spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="6665f-109">Tipi di eventi dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6665f-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="6665f-110">Impostazioni di accesso allo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6665f-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="6665f-111">Autorizzazioni predefinite per gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="6665f-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6665f-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="6665f-113">Sicurezza dello spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-113">WMI Namespace Security</span></span>

<span data-ttu-id="6665f-114">WMI mantiene la sicurezza dello spazio dei nomi confrontando il [*token di accesso*](/windows/desktop/SecGloss/a-gly) dell'utente che si connette allo spazio dei nomi con il [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="6665f-115">Per ulteriori informazioni sulla sicurezza di Windows, vedere [accesso a oggetti a protezione diretta WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="6665f-116">Tenere presente che, a partire da Windows Vista, [controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) influisca sull'accesso ai dati WMI e su cosa può essere configurato con il [*controllo WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="6665f-117">Per ulteriori informazioni, vedere [autorizzazioni predefinite per gli spazi dei nomi WMI](#default-permissions-on-wmi-namespaces) e [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="6665f-118">L'accesso agli spazi dei nomi WMI viene inoltre influenzato quando la connessione è da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="6665f-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="6665f-119">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md), [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)e [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="6665f-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="6665f-120">I provider devono basarsi sull'impostazione di rappresentazione per la connessione per determinare se lo script client o l'applicazione deve ricevere dati.</span><span class="sxs-lookup"><span data-stu-id="6665f-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="6665f-121">Per ulteriori informazioni sullo script e sulle applicazioni client, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="6665f-122">Per ulteriori informazioni sulla rappresentazione del [*provider*](gloss-p.md) , vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="6665f-123">Controllo dello spazio dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="6665f-124">WMI utilizza lo spazio dei nomi [*elenchi di controllo di accesso di sistema (SACL)*](/windows/desktop/SecGloss/s-gly) per controllare l'attività dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6665f-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="6665f-125">Per abilitare il controllo degli spazi dei nomi WMI, utilizzare la scheda **sicurezza** del [*controllo WMI*](gloss-w.md) per modificare le impostazioni di controllo per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="6665f-126">Il controllo non è abilitato durante l'installazione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6665f-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="6665f-127">Per abilitare il controllo, fare clic sulla scheda **controllo** nella finestra **sicurezza** standard.</span><span class="sxs-lookup"><span data-stu-id="6665f-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="6665f-128">È quindi possibile aggiungere una voce di controllo.</span><span class="sxs-lookup"><span data-stu-id="6665f-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="6665f-129">Criteri di gruppo per il computer locale deve essere impostato in modo da consentire il controllo.</span><span class="sxs-lookup"><span data-stu-id="6665f-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="6665f-130">Per abilitare il controllo, è possibile eseguire lo snap-in MMC gpedit. msc e impostare **controllo accesso oggetti** in **Configurazione computer** impostazioni di Windows impostazioni di sicurezza Criteri di  >    >    >    >  **controllo** locali.</span><span class="sxs-lookup"><span data-stu-id="6665f-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="6665f-131">Una voce di controllo modifica l'elenco SACL dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="6665f-132">Quando si aggiunge una voce di controllo, si tratta di un utente, un gruppo, un computer o un'entità di sicurezza predefinita.</span><span class="sxs-lookup"><span data-stu-id="6665f-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="6665f-133">Dopo aver aggiunto la voce, è possibile impostare le operazioni di accesso che generano eventi del registro di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6665f-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="6665f-134">Ad esempio, per il gruppo Authenticated Users, è possibile fare clic su Execute methods.</span><span class="sxs-lookup"><span data-stu-id="6665f-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="6665f-135">Questa impostazione determina gli eventi del registro di sicurezza ogni volta che un membro del gruppo Authenticated Users esegue un metodo nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="6665f-136">L'ID evento per gli eventi WMI è 4662.</span><span class="sxs-lookup"><span data-stu-id="6665f-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="6665f-137">Per modificare le impostazioni di controllo, l'account deve appartenere al gruppo Administrators ed essere in esecuzione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="6665f-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="6665f-138">L'account Administrator predefinito può anche modificare la sicurezza o il controllo per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="6665f-139">Per ulteriori informazioni sull'esecuzione in modalità con privilegi elevati, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="6665f-140">Il controllo WMI genera eventi di esito positivo o negativo per i tentativi di accesso agli spazi dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="6665f-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="6665f-141">Il servizio non controlla l'esito positivo o negativo delle operazioni del provider.</span><span class="sxs-lookup"><span data-stu-id="6665f-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="6665f-142">Ad esempio, quando uno script si connette a WMI e a uno spazio dei nomi, potrebbe non riuscire perché l'account con cui viene eseguito lo script non ha accesso a tale spazio dei nomi o può tentare di eseguire un'operazione, ad esempio la modifica del DACL, non concesso.</span><span class="sxs-lookup"><span data-stu-id="6665f-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="6665f-143">Se si esegue un account nel gruppo Administrators, è possibile visualizzare gli eventi di controllo dello spazio dei nomi nell'interfaccia utente di **Visualizzatore eventi** .</span><span class="sxs-lookup"><span data-stu-id="6665f-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="6665f-144">Tipi di eventi dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6665f-144">Types of Namespace Events</span></span>

<span data-ttu-id="6665f-145">WMI traccia i tipi di eventi seguenti nel registro eventi di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="6665f-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="6665f-146">Controllo riuscito</span><span class="sxs-lookup"><span data-stu-id="6665f-146">Audit Success</span></span>

    <span data-ttu-id="6665f-147">L'operazione deve completare due passaggi per un controllo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="6665f-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="6665f-148">In primo luogo, WMI concede l'accesso all'applicazione client o allo script in base al SID client e all'elenco DACL dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6665f-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="6665f-149">In secondo luogo, l'operazione richiesta corrisponde ai diritti di accesso nel SACL dello spazio dei nomi per tale utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="6665f-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="6665f-150">Controllo non riuscito</span><span class="sxs-lookup"><span data-stu-id="6665f-150">Audit Failure</span></span>

    <span data-ttu-id="6665f-151">WMI nega l'accesso allo spazio dei nomi, ma l'operazione richiesta corrisponde ai diritti di accesso nel SACL dello spazio dei nomi per tale utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="6665f-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="6665f-152">Impostazioni di accesso allo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6665f-152">Namespace Access Settings</span></span>

<span data-ttu-id="6665f-153">È possibile visualizzare i diritti di accesso allo spazio dei nomi per diversi account nel controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="6665f-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="6665f-154">Queste costanti sono descritte in [**costanti di diritti di accesso allo spazio dei nomi**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="6665f-155">È possibile modificare l'accesso a uno spazio dei nomi WMI utilizzando il controllo WMI o a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="6665f-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="6665f-156">Per ulteriori informazioni, vedere [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="6665f-157">WMI controlla le modifiche apportate a tutte le autorizzazioni di accesso elencate nell'elenco seguente, ad eccezione dell'autorizzazione Abilita remota.</span><span class="sxs-lookup"><span data-stu-id="6665f-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="6665f-158">Le modifiche vengono registrate come controllo riuscito o errore corrispondente all'autorizzazione Modifica sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6665f-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="6665f-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Metodi Execute</span><span class="sxs-lookup"><span data-stu-id="6665f-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="6665f-160">Consente all'utente di eseguire metodi definiti nelle classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6665f-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="6665f-161">Corrisponde alla costante di autorizzazione per l' **\_ \_ esecuzione del metodo WBEM** .</span><span class="sxs-lookup"><span data-stu-id="6665f-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Scrittura completa</span><span class="sxs-lookup"><span data-stu-id="6665f-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="6665f-163">Consente l'accesso completo in lettura, scrittura ed eliminazione alle classi e alle istanze di classi WMI, sia statiche che dinamiche.</span><span class="sxs-lookup"><span data-stu-id="6665f-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="6665f-164">Corrisponde alla costante di autorizzazione per l'accesso alla **\_ \_ \_ Rep Full Write di WBEM** .</span><span class="sxs-lookup"><span data-stu-id="6665f-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Scrittura parziale</span><span class="sxs-lookup"><span data-stu-id="6665f-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="6665f-166">Consente l'accesso in scrittura alle istanze di classi WMI statiche.</span><span class="sxs-lookup"><span data-stu-id="6665f-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="6665f-167">Corrisponde alla costante di autorizzazione per l'accesso con **\_ \_ scrittura \_ parziale WBEM** .</span><span class="sxs-lookup"><span data-stu-id="6665f-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Scrittura del provider</span><span class="sxs-lookup"><span data-stu-id="6665f-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="6665f-169">Consente l'accesso in scrittura alle istanze di classi WMI dinamiche.</span><span class="sxs-lookup"><span data-stu-id="6665f-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="6665f-170">Corrisponde alla costante di autorizzazione di accesso del **\_ \_ provider di scrittura WBEM** .</span><span class="sxs-lookup"><span data-stu-id="6665f-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Abilita account</span><span class="sxs-lookup"><span data-stu-id="6665f-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="6665f-172">Consente l'accesso in lettura alle istanze della classe WMI.</span><span class="sxs-lookup"><span data-stu-id="6665f-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="6665f-173">Corrisponde alla costante di autorizzazione **\_ abilitata** per l'accesso WBEM.</span><span class="sxs-lookup"><span data-stu-id="6665f-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Abilita remoto</span><span class="sxs-lookup"><span data-stu-id="6665f-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="6665f-175">Consente l'accesso allo spazio dei nomi da parte dei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="6665f-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="6665f-176">Corrisponde alla costante di autorizzazione per l'accesso **\_ \_ remoto WBEM** .</span><span class="sxs-lookup"><span data-stu-id="6665f-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sicurezza di lettura</span><span class="sxs-lookup"><span data-stu-id="6665f-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="6665f-178">Consente l'accesso in sola lettura alle impostazioni DACL.</span><span class="sxs-lookup"><span data-stu-id="6665f-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="6665f-179">Corrisponde alla costante di autorizzazione per l'accesso al **\_ controllo Read** .</span><span class="sxs-lookup"><span data-stu-id="6665f-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="6665f-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Modifica sicurezza</span><span class="sxs-lookup"><span data-stu-id="6665f-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="6665f-181">Consente l'accesso in scrittura alle impostazioni DACL.</span><span class="sxs-lookup"><span data-stu-id="6665f-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="6665f-182">Corrisponde alla costante di autorizzazione per l'accesso alla **\_ DAC di scrittura** .</span><span class="sxs-lookup"><span data-stu-id="6665f-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="6665f-183">Autorizzazioni predefinite per gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="6665f-184">I gruppi di sicurezza predefiniti sono:</span><span class="sxs-lookup"><span data-stu-id="6665f-184">The default security groups are:</span></span>

-   <span data-ttu-id="6665f-185">Utenti autenticati</span><span class="sxs-lookup"><span data-stu-id="6665f-185">Authenticated Users</span></span>
-   <span data-ttu-id="6665f-186">LOCAL SERVICE</span><span class="sxs-lookup"><span data-stu-id="6665f-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="6665f-187">NETWORK SERVICE</span><span class="sxs-lookup"><span data-stu-id="6665f-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="6665f-188">Amministratori (nel computer locale)</span><span class="sxs-lookup"><span data-stu-id="6665f-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="6665f-189">Le autorizzazioni di accesso predefinite per gli utenti, il servizio locale e il servizio di rete autenticato sono:</span><span class="sxs-lookup"><span data-stu-id="6665f-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="6665f-190">Esegui metodi</span><span class="sxs-lookup"><span data-stu-id="6665f-190">Execute Methods</span></span>
-   <span data-ttu-id="6665f-191">Scrittura completa</span><span class="sxs-lookup"><span data-stu-id="6665f-191">Full Write</span></span>
-   <span data-ttu-id="6665f-192">Abilita account</span><span class="sxs-lookup"><span data-stu-id="6665f-192">Enable Account</span></span>

<span data-ttu-id="6665f-193">Gli account del gruppo Administrators dispongono di tutti i diritti disponibili, inclusa la modifica dei descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6665f-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="6665f-194">Tuttavia, a causa del controllo dell'account utente, il controllo WMI o lo script deve essere eseguito con privilegi elevati di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6665f-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="6665f-195">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="6665f-196">In alcuni casi uno script o un'applicazione deve abilitare un privilegio di amministratore, ad esempio **SeSecurityPrivilege**, per eseguire un'operazione.</span><span class="sxs-lookup"><span data-stu-id="6665f-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="6665f-197">Uno script può ad esempio eseguire il metodo [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) senza **SeSecurityPrivilege** e ottenere le informazioni di sicurezza nell'elenco di [*controllo di accesso discrezionale (DACL)*](/windows/desktop/SecGloss/d-gly) del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto Printer.</span><span class="sxs-lookup"><span data-stu-id="6665f-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="6665f-198">Tuttavia, le informazioni relative al SACL non vengono restituite allo script, a meno che il privilegio **SeSecurityPrivilege** non sia disponibile e abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="6665f-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="6665f-199">Se per l'account non è disponibile il privilegio, non è possibile abilitarlo.</span><span class="sxs-lookup"><span data-stu-id="6665f-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="6665f-200">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6665f-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6665f-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6665f-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6665f-202">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="6665f-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
