---
description: Un'applicazione COM+ è essenzialmente un costrutto dichiarativo che consente di configurare un numero qualsiasi di componenti in comune. È ad esempio possibile configurare i componenti di un'applicazione con criteri di sicurezza comuni.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurazione di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304633"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="e46a0-104">Configurazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="e46a0-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="e46a0-105">Un'applicazione COM+ è essenzialmente un costrutto dichiarativo che consente di configurare un numero qualsiasi di componenti in comune.</span><span class="sxs-lookup"><span data-stu-id="e46a0-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="e46a0-106">È ad esempio possibile configurare i componenti di un'applicazione con criteri di sicurezza comuni.</span><span class="sxs-lookup"><span data-stu-id="e46a0-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="e46a0-107">La configurazione è una parte essenziale del processo di sviluppo per le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="e46a0-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="e46a0-108">La modalità di configurazione di un'applicazione determinerà il modo in cui COM+ fornirà servizi e il suo comportamento durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="e46a0-109">È possibile configurare le applicazioni COM+ utilizzando lo strumento di amministrazione Servizi componenti o gli oggetti e le interfacce di amministrazione con script che forniscono la funzionalità sottostante dello strumento di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="e46a0-110">Per informazioni dettagliate sull'esecuzione di amministrazione con script, vedere [automazione di com+ Administration](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="e46a0-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="e46a0-111">È possibile configurare gli elementi ai livelli seguenti all'interno delle applicazioni COM+:</span><span class="sxs-lookup"><span data-stu-id="e46a0-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="e46a0-112">Impostazioni a livello di applicazione</span><span class="sxs-lookup"><span data-stu-id="e46a0-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="e46a0-113">Impostazioni a livello di componente (a livello di classe)</span><span class="sxs-lookup"><span data-stu-id="e46a0-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="e46a0-114">Impostazione a livello di interfaccia</span><span class="sxs-lookup"><span data-stu-id="e46a0-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="e46a0-115">Impostazione a livello di metodo</span><span class="sxs-lookup"><span data-stu-id="e46a0-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="e46a0-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e46a0-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="e46a0-117">La modalità di installazione dei componenti in un'applicazione può influire sul modo in cui è possibile configurarle.</span><span class="sxs-lookup"><span data-stu-id="e46a0-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="e46a0-118">È necessario installare sempre i componenti in applicazioni COM+, anziché importarli.</span><span class="sxs-lookup"><span data-stu-id="e46a0-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="e46a0-119">L'installazione dei componenti li registrerà completamente, insieme alle interfacce e alle librerie dei tipi, nel database di registrazione della classe COM+ (RegDB) in modo che sia possibile configurarli.</span><span class="sxs-lookup"><span data-stu-id="e46a0-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="e46a0-120">Impostazioni Application-Level</span><span class="sxs-lookup"><span data-stu-id="e46a0-120">Application-Level Settings</span></span>



| <span data-ttu-id="e46a0-121">Attributo</span><span class="sxs-lookup"><span data-stu-id="e46a0-121">Attribute</span></span>                                                                                        | <span data-ttu-id="e46a0-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46a0-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e46a0-123">Activation</span><span class="sxs-lookup"><span data-stu-id="e46a0-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="e46a0-124">Specifica il tipo di applicazione, ovvero applicazione server o applicazione libreria.</span><span class="sxs-lookup"><span data-stu-id="e46a0-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e46a0-125">Abilitazione di controlli di accesso</span><span class="sxs-lookup"><span data-stu-id="e46a0-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="e46a0-126">Attiva e disattiva il controllo della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e46a0-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="e46a0-127">Livello di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e46a0-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="e46a0-128">Specifica che i controlli di accesso verranno eseguiti a livello di processo (livelli di controllo di accesso generati da ruoli) o sia a livello di processo che a livello di componente (sicurezza completa basata sui ruoli).</span><span class="sxs-lookup"><span data-stu-id="e46a0-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="e46a0-129">Livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="e46a0-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="e46a0-130">Imposta il livello di autenticazione utilizzato per le chiamate nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e46a0-131">Livello di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="e46a0-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="e46a0-132">Imposta il livello di rappresentazione usato per le chiamate ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e46a0-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e46a0-133">Accodamento</span><span class="sxs-lookup"><span data-stu-id="e46a0-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="e46a0-134">Specifica che i componenti dell'applicazione utilizzeranno i servizi di Accodamento.</span><span class="sxs-lookup"><span data-stu-id="e46a0-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="e46a0-135">Abilita CRM</span><span class="sxs-lookup"><span data-stu-id="e46a0-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="e46a0-136">Consente l'uso di gestione risorse di compensazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="e46a0-137">Eseguire l'applicazione come servizio</span><span class="sxs-lookup"><span data-stu-id="e46a0-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="e46a0-138">Configura e implementa un'applicazione server COM+ come servizio NT.</span><span class="sxs-lookup"><span data-stu-id="e46a0-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e46a0-139">Servizio SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="e46a0-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="e46a0-140">Espone un'applicazione COM+ come un servizio Web XML.</span><span class="sxs-lookup"><span data-stu-id="e46a0-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="e46a0-141">Pool di applicazioni</span><span class="sxs-lookup"><span data-stu-id="e46a0-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="e46a0-142">Aggiunge la scalabilità per i processi a thread singolo e si integra con il servizio di riciclo delle applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="e46a0-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="e46a0-143">Riciclo delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="e46a0-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="e46a0-144">Aumenta la stabilità dell'applicazione arrestando normalmente un processo associato a un'applicazione e riavviarlo.</span><span class="sxs-lookup"><span data-stu-id="e46a0-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="e46a0-145">Dump del processo</span><span class="sxs-lookup"><span data-stu-id="e46a0-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="e46a0-146">Esegue il dump dell'intero stato di un processo senza terminarlo a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="e46a0-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="e46a0-147">Arresto del processo server</span><span class="sxs-lookup"><span data-stu-id="e46a0-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="e46a0-148">Arresta un processo dopo un periodo di inattività specificato.</span><span class="sxs-lookup"><span data-stu-id="e46a0-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e46a0-149">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="e46a0-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="e46a0-150">Disabilita le modifiche apportate alle impostazioni di configurazione, inclusa l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e46a0-151">Identità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e46a0-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="e46a0-152">Specifica l'identità con cui viene eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="e46a0-153">Avvia nel debugger</span><span class="sxs-lookup"><span data-stu-id="e46a0-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="e46a0-154">Specifica che l'applicazione verrà avviata in un debugger, con le impostazioni della riga di comando specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="e46a0-155">Abilita supporto 3GB</span><span class="sxs-lookup"><span data-stu-id="e46a0-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="e46a0-156">Consente l'uso dello spazio degli indirizzi di memoria del processo esteso.</span><span class="sxs-lookup"><span data-stu-id="e46a0-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="e46a0-157">Impostazioni di Component-Level (a livello di classe)</span><span class="sxs-lookup"><span data-stu-id="e46a0-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e46a0-158">Attributo</span><span class="sxs-lookup"><span data-stu-id="e46a0-158">Attribute</span></span></th>
<th><span data-ttu-id="e46a0-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46a0-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e46a0-160"><a href="configuring-transactions.md">Transazioni</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-161">Imposta i requisiti di transazione automatici disabilitati, non supportati, supportati, necessari o nuovi.</span><span class="sxs-lookup"><span data-stu-id="e46a0-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46a0-162"><a href="setting-the-synchronization-attribute.md">Sincronizzazione</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-163">Imposta i requisiti di sincronizzazione disabilitati, non supportati, supportati, necessari o nuovi.</span><span class="sxs-lookup"><span data-stu-id="e46a0-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46a0-164"><a href="enabling-jit-activation-for-a-component.md">Attivazione JIT</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-165">Abilita l'attivazione JIT.</span><span class="sxs-lookup"><span data-stu-id="e46a0-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46a0-166"><a href="configuring-a-component-to-be-pooled.md">Pooling di oggetti</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-167">Abilita il pool di oggetti.</span><span class="sxs-lookup"><span data-stu-id="e46a0-167">Enables object pooling.</span></span> <span data-ttu-id="e46a0-168">Le dimensioni minime e massime del pool e i valori di timeout dell'oggetto sono configurabili.</span><span class="sxs-lookup"><span data-stu-id="e46a0-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46a0-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Costruzione di oggetti</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-170">Consente la costruzione di oggetti con parametri con una stringa del costruttore specificata amministrativamente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e46a0-171">La stringa del costruttore non deve essere utilizzata per archiviare informazioni sensibili alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e46a0-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46a0-172"><a href="enabling-access-checks-at-the-component-level.md">Controlli di accesso a livello di componente</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-173">Attiva o disattiva il controllo di sicurezza basato sui ruoli a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46a0-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Assegnazione di ruolo dichiarativa</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-175">Consente l'assegnazione esplicita dei ruoli al componente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46a0-176"><a href="persistent-client-side-failures.md">Classe Exception di Accodamento</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-177">Indica una classe di eccezioni per la gestione degli errori sul lato client.</span><span class="sxs-lookup"><span data-stu-id="e46a0-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46a0-178"><a href="com--instrumentation-concepts.md">Eventi e statistiche di strumentazione</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-179">Consente di creare report dettagliati sugli eventi di sistema e sulle statistiche degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="e46a0-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e46a0-180"><a href="context-activation.md">Contesto di attivazione</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-181">Abilita l'attivazione forzata di un oggetto nel contesto del chiamante o nel contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="e46a0-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e46a0-182"><a href="what-s-new-in-com--1-5.md">Creazione di componenti privati</a></span><span class="sxs-lookup"><span data-stu-id="e46a0-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="e46a0-183">Contrassegna il componente come privato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-183">Marks component as private to the application.</span></span> <span data-ttu-id="e46a0-184">Un componente privato può essere visualizzato e attivato solo da altri componenti nella stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="e46a0-185">Impostazione Interface-Level</span><span class="sxs-lookup"><span data-stu-id="e46a0-185">Interface-Level Setting</span></span>



| <span data-ttu-id="e46a0-186">Attributo</span><span class="sxs-lookup"><span data-stu-id="e46a0-186">Attribute</span></span>                                                                                           | <span data-ttu-id="e46a0-187">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46a0-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e46a0-188">Queued</span><span class="sxs-lookup"><span data-stu-id="e46a0-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="e46a0-189">Indica un'interfaccia accodabile, definita in IDL.</span><span class="sxs-lookup"><span data-stu-id="e46a0-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="e46a0-190">Assegnazione di ruolo dichiarativa</span><span class="sxs-lookup"><span data-stu-id="e46a0-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="e46a0-191">Consente l'assegnazione esplicita dei ruoli all'interfaccia, oltre ai ruoli ereditati in modo implicito dal livello del componente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="e46a0-192">Impostazione Method-Level</span><span class="sxs-lookup"><span data-stu-id="e46a0-192">Method-Level Setting</span></span>



| <span data-ttu-id="e46a0-193">Attributo</span><span class="sxs-lookup"><span data-stu-id="e46a0-193">Attribute</span></span>                                                                                           | <span data-ttu-id="e46a0-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e46a0-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e46a0-195">Operazione eseguita automaticamente</span><span class="sxs-lookup"><span data-stu-id="e46a0-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="e46a0-196">Disattiva automaticamente l'oggetto al ritorno del metodo e i voti nella transazione.</span><span class="sxs-lookup"><span data-stu-id="e46a0-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="e46a0-197">Assegnazione di ruolo dichiarativa</span><span class="sxs-lookup"><span data-stu-id="e46a0-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="e46a0-198">Consente l'assegnazione esplicita dei ruoli al metodo, nonché i ruoli ereditati in modo implicito dai livelli di interfaccia e di componente.</span><span class="sxs-lookup"><span data-stu-id="e46a0-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e46a0-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e46a0-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e46a0-200">Automazione dell'amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="e46a0-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="e46a0-201">Creazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="e46a0-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e46a0-202">Distribuzione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="e46a0-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




