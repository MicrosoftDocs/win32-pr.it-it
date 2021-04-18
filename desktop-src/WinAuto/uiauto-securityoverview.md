---
title: Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato
description: Le tecnologie per l'accesso facilitato sono applicazioni eseguite sul desktop di Windows e consentono agli utenti di accedere all'accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente di Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- attributo uiAccess
- Automazione interfaccia utente, attributo uiAccess
- sicurezza, attributo uiAccess
- Tag requestedExecutionLevel
- Automazione interfaccia utente, tag requestedExecutionLevel
- Automazione interfaccia utente, considerazioni sulla sicurezza
- Automazione interfaccia utente, file manifesto
- file manifesto
- controllo dell'account utente
- sicurezza, controllo dell'account utente
- sicurezza, file manifesto
- sicurezza, tag requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2020
ms.locfileid: "106300641"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="1d3bb-115">Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="1d3bb-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="1d3bb-116">Le tecnologie per l'accesso facilitato sono applicazioni eseguite sul desktop di Windows e consentono agli utenti di accedere all'accessibilità di interagire con il sistema operativo e altre applicazioni in esecuzione nel computer, incluse le applicazioni nella nuova interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="1d3bb-117">Le applicazioni di Assistive Technology funzionano recuperando le informazioni dal sistema operativo e da altre applicazioni, quindi presentando le informazioni in modo che siano accessibili all'utente.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="1d3bb-118">Un'applicazione di Assistive Technology può anche "guidare" a livello di codice il sistema operativo e altre applicazioni in base all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="1d3bb-119">La natura delle applicazioni per la tecnologia per l'accessibilità richiede il superamento dei limiti del processo e l'accesso ai processi che vengono eseguiti a un livello di integrità superiore (IL).</span><span class="sxs-lookup"><span data-stu-id="1d3bb-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="1d3bb-120">Un'applicazione per la tecnologia per l'accessibilità viene eseguita a media IL. Ad esempio, quando l'utente tenta di eseguire un'attività che richiede privilegi amministrativi, Windows visualizza una finestra di dialogo in cui viene chiesto all'utente di fornire il consenso per continuare.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="1d3bb-121">Questa finestra di dialogo viene eseguita con un livello di integrità superiore per proteggerla dalla comunicazione tra processi, in modo che IL software dannoso non possa simulare l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="1d3bb-122">Analogamente, la schermata di accesso al desktop viene eseguita con un livello di integrità superiore per impedire l'accesso da parte di altri processi.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="1d3bb-123">In genere, le applicazioni di Assistive Technology necessitano dell'accesso agli elementi dell'interfaccia utente del sistema protetto o ad altri processi che potrebbero essere in esecuzione a un livello di privilegi più elevato.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="1d3bb-124">Pertanto, le applicazioni di Assistive Technology devono essere considerate attendibili dal sistema e devono essere eseguite con privilegi speciali.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="1d3bb-125">Per ottenere l'accesso a processi IL più elevati, un'applicazione di Assistive Technology deve impostare il flag UIAccess nel manifesto dell'applicazione ed essere avviata da un utente con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="1d3bb-126">I privilegi di accesso sono limitati come segue:</span><span class="sxs-lookup"><span data-stu-id="1d3bb-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="1d3bb-127">Un'applicazione che non dispone di UIAccess nel manifesto inizia con IL media IL e non può accedere all'interfaccia utente del processo con privilegi elevati ("medium +" IL).</span><span class="sxs-lookup"><span data-stu-id="1d3bb-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="1d3bb-128">Un'applicazione con UIAccess nel manifesto e avviata da un utente non appartenente al gruppo Administrators, viene avviata come IL "medio +" e non può accedere all'interfaccia utente con privilegi elevati (nessun elemento in esecuzione come "alto", ad esempio le app avviate tramite un **clic con il pulsante destro del mouse su > eseguito come amministratore**).</span><span class="sxs-lookup"><span data-stu-id="1d3bb-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="1d3bb-129">Un'applicazione dispone di accesso all'interfaccia utente e viene avviata da un utente amministratore avviata come IL "alto" e può accedere all'interfaccia utente con privilegi elevati perché ha lo stesso linguaggio IL.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="1d3bb-130">UIAccess non è sufficiente per consentire a un processo di spostarsi verso l'alto attraverso il limite IL.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="1d3bb-131">Oltre ad accedere ai processi IL più elevati, un'applicazione di Assistive Technology con questi privilegi può essere eseguita come applicazione in primo piano nell'ordine z in qualsiasi momento, vale a dire che un'applicazione Assistive Technology può essere visibile e disponibile ogni volta che l'utente lo richiede.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="1d3bb-132">Nessuno degli scenari precedentemente elencati fornisce l'accesso all'interfaccia utente in esecuzione nel sistema IL.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="1d3bb-133">Questa operazione è possibile solo se il processo viene avviato nel desktop del controllo dell'account utente (UAC) in SYSTEM (e System IL).</span><span class="sxs-lookup"><span data-stu-id="1d3bb-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="1d3bb-134">In questo caso, l'impostazione di UIAccess non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="1d3bb-135">Requisiti UIAccess per le applicazioni di Assistive Technology</span><span class="sxs-lookup"><span data-stu-id="1d3bb-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="1d3bb-136">Un'applicazione di Assistive Technology è un'applicazione desktop Windows Windows che interagisce con altri processi in esecuzione sul desktop e nella nuova interfaccia utente di Windows per ottenere informazioni dal sistema e dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="1d3bb-137">L'applicazione Assistive Technology può quindi fornire le informazioni agli utenti di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="1d3bb-138">Un'applicazione Assistive Technology Ottiene l'accesso ad altri processi impostando il flag UIAccess nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="1d3bb-139">Per usare il flag UIAccess, un'applicazione di Assistive Technology deve soddisfare i requisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="1d3bb-140">È necessario visualizzare, interagire o riflettere le informazioni di un'altra applicazione per fornire informazioni per uno scenario di accessibilità e/o</span><span class="sxs-lookup"><span data-stu-id="1d3bb-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="1d3bb-141">Richiedere l'esecuzione come finestra in primo piano per ottenere o visualizzare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="1d3bb-142">Per usare UIAccess, un'applicazione di Assistive Technology deve:</span><span class="sxs-lookup"><span data-stu-id="1d3bb-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="1d3bb-143">Essere firmato con un certificato per interagire con le applicazioni in esecuzione con un livello di privilegi più elevato.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="1d3bb-144">Essere considerato attendibile dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-144">Be trusted by the system.</span></span> <span data-ttu-id="1d3bb-145">L'applicazione deve essere installata in un percorso sicuro che richiede l'accesso a una richiesta di controllo dell'account utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="1d3bb-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="1d3bb-146">Ad esempio, la cartella Program Files.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="1d3bb-147">Essere compilato con un file manifesto che include il flag uiAccess.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="1d3bb-148">UIAccess non deve essere utilizzato:</span><span class="sxs-lookup"><span data-stu-id="1d3bb-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="1d3bb-149">Da applicazioni che non sono tecnologie per l'accesso facilitato.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="1d3bb-150">Da applicazioni tecnologiche che consentono di visualizzare informazioni o interfaccia utente non rilevanti per lo scenario di accessibilità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="1d3bb-151">Per le applicazioni che vogliono solo apparire sopra le altre applicazioni nella nuova interfaccia utente di Windows.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="1d3bb-152">Le applicazioni sviluppate per la nuova interfaccia utente di Windows non dispongono di UIAccess come opzione disponibile.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="1d3bb-153">Impostazione di UIAccess nel file manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1d3bb-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="1d3bb-154">Per accedere all'interfaccia utente del sistema protetto, le applicazioni devono essere compilate con un file manifesto che include un attributo speciale nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="1d3bb-155">Questo attributo **uiAccess** è incluso nel tag **requestedExecutionLevel** , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="1d3bb-156">Il valore dell'attributo **Level** in questo codice è solo un esempio.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="1d3bb-157">Per impostazione predefinita, **uiAccess** è "false".</span><span class="sxs-lookup"><span data-stu-id="1d3bb-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="1d3bb-158">Se l'attributo viene omesso o se non è presente alcun manifesto, l'applicazione non può accedere all'interfaccia utente protetta.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="1d3bb-159">Per ulteriori informazioni sulla sicurezza di Windows, sulla firma delle applicazioni e sulla creazione di manifesti, vedere [la storia degli sviluppatori di Windows Vista e Windows Server 2008: requisiti per lo sviluppo di applicazioni Windows Vista per il controllo dell'account utente](/previous-versions/aa905330(v=msdn.10)) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="1d3bb-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d3bb-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d3bb-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d3bb-161">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="1d3bb-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 