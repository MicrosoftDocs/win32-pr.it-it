---
title: Traccia eventi in ADSI
description: Windows Server 2008 e Windows Vista introducono la traccia eventi in Active Directory Service Interfaces (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300424"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="81dca-104">Traccia eventi in ADSI</span><span class="sxs-lookup"><span data-stu-id="81dca-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="81dca-105">Windows Server 2008 e Windows Vista introducono la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="81dca-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="81dca-106">Alcune aree del provider LDAP ADSI hanno un'implementazione sottostante complessa o che prevede una sequenza di passaggi che rendono difficile la diagnosi dei problemi.</span><span class="sxs-lookup"><span data-stu-id="81dca-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="81dca-107">Per consentire agli sviluppatori di applicazioni di risolvere i problemi, è stata aggiunta la traccia eventi alle aree seguenti:</span><span class="sxs-lookup"><span data-stu-id="81dca-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="81dca-108">Analisi dello schema e download</span><span class="sxs-lookup"><span data-stu-id="81dca-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="81dca-109">Per l'interfaccia IADs in ADSI è necessario che lo schema LDAP venga memorizzato nella cache del client in modo che sia possibile effettuare il marshalling degli attributi correttamente (come descritto nel [modello di schema ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="81dca-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="81dca-110">A tale scopo, ADSI carica lo schema per ogni processo (e per ogni server/dominio LDAP) in memoria da un file di schema (SCH) salvato nel disco locale o dal server LDAP.</span><span class="sxs-lookup"><span data-stu-id="81dca-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="81dca-111">Diversi processi nello stesso computer client utilizzano lo schema memorizzato nella cache su disco, se disponibile e applicabile.</span><span class="sxs-lookup"><span data-stu-id="81dca-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="81dca-112">Se non è possibile ottenere lo schema dal disco o dal server, ADSI usa uno schema predefinito hardcoded.</span><span class="sxs-lookup"><span data-stu-id="81dca-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="81dca-113">Quando si verifica questa situazione, non è possibile effettuare il marshalling degli attributi che non fanno parte di questo schema predefinito e ADSI restituisce un errore durante il recupero di questi attributi.</span><span class="sxs-lookup"><span data-stu-id="81dca-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="81dca-114">Una serie di fattori può causare questa situazione, inclusi i problemi di analisi dello schema e privilegi insufficienti per scaricare lo schema.</span><span class="sxs-lookup"><span data-stu-id="81dca-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="81dca-115">Spesso è difficile determinare il motivo per cui viene utilizzato un determinato schema predefinito.</span><span class="sxs-lookup"><span data-stu-id="81dca-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="81dca-116">L'uso della traccia eventi in quest'area consente di diagnosticare più rapidamente il problema e risolverlo.</span><span class="sxs-lookup"><span data-stu-id="81dca-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="81dca-117">Modifica e impostazione della password</span><span class="sxs-lookup"><span data-stu-id="81dca-117">Changing and Setting the Password</span></span>

<span data-ttu-id="81dca-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**password**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) impiegano più di un meccanismo per eseguire l'operazione richiesta in base alla configurazione disponibile, come descritto in [impostazione e modifica delle password utente con il provider LDAP](setting-user-passwords-for-ldap-providers.md).</span><span class="sxs-lookup"><span data-stu-id="81dca-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="81dca-119">Quando **ChangePassword** e **sepassword** hanno esito negativo, può essere difficile determinare esattamente il motivo per cui la traccia eventi aiuterà a risolvere i problemi con questi metodi.</span><span class="sxs-lookup"><span data-stu-id="81dca-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="81dca-120">Cache di binding ADSI</span><span class="sxs-lookup"><span data-stu-id="81dca-120">ADSI Bind Cache</span></span>

<span data-ttu-id="81dca-121">ADSI tenta internamente di riutilizzare le connessioni LDAP laddove possibile (vedere [caching della connessione](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="81dca-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="81dca-122">Quando si esegue la risoluzione dei problemi, è utile tracciare se è stata aperta una nuova connessione per la comunicazione con il server o se è stata utilizzata una connessione esistente.</span><span class="sxs-lookup"><span data-stu-id="81dca-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="81dca-123">Può anche essere utile per tenere traccia del ciclo di vita della cache di connessione (talvolta definita cache di binding) e della relativa creazione o chiusura e se è stato rilevato un riferimento alla connessione.</span><span class="sxs-lookup"><span data-stu-id="81dca-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="81dca-124">Nel caso di un' [associazione senza server](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI chiama il localizzatore DC per selezionare un server per il dominio del contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="81dca-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="81dca-125">ADSI gestisce quindi una cache del mapping del server di dominio per le connessioni successive.</span><span class="sxs-lookup"><span data-stu-id="81dca-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="81dca-126">La traccia eventi consente di tracciare la selezione del controller di dominio ed è quindi utile per la risoluzione dei problemi relativi alla connessione.</span><span class="sxs-lookup"><span data-stu-id="81dca-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="81dca-127">Abilitazione della traccia e avvio di una sessione di traccia</span><span class="sxs-lookup"><span data-stu-id="81dca-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="81dca-128">Per attivare la traccia ADSI, creare la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="81dca-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="81dca-129">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ ***ProcessName***</span><span class="sxs-lookup"><span data-stu-id="81dca-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="81dca-130">*ProcessName* è il nome completo del processo che si desidera tracciare, inclusa la relativa estensione, ad esempio "Svchost.exe".</span><span class="sxs-lookup"><span data-stu-id="81dca-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="81dca-131">Inoltre, è possibile inserire un valore facoltativo di tipo **DWORD** denominato PID in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="81dca-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="81dca-132">È consigliabile impostare questo valore e quindi tracciare solo un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="81dca-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="81dca-133">In caso contrario, verranno tracciate tutte le istanze dell'applicazione specificata da *ProcessName* .</span><span class="sxs-lookup"><span data-stu-id="81dca-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="81dca-134">Eseguire quindi il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="81dca-134">Then execute the following command:</span></span>

<span data-ttu-id="81dca-135">**tracelog.exe-avviare** *sessionname*  \* *-GUID \# \* \* \* \_ GUID del provider* **-f** *filename* **-flag** *flag* **-Level** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="81dca-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="81dca-136">*sessionname* è semplicemente un identificatore arbitrario utilizzato per etichettare la sessione di traccia. quando si arresta la sessione di traccia, sarà necessario fare riferimento al nome della sessione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="81dca-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="81dca-137">Il GUID del provider di rilevamento ADSI è "7288c9f8-D63C-4932-A345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="81dca-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="81dca-138">*filename* specifica il file di log in cui verranno scritti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="81dca-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="81dca-139">*flag* deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="81dca-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="81dca-140">**SCHEMA di DEBUG \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="81dca-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="81dca-141">0x00000001</span></span><br/> |
| <span data-ttu-id="81dca-142">**CHANGEPWD di DEBUG \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="81dca-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="81dca-143">0x00000002</span></span><br/> |
| <span data-ttu-id="81dca-144">**Setpwd di DEBUG \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="81dca-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="81dca-145">0x00000004</span></span><br/> |
| <span data-ttu-id="81dca-146">**BINDCACHE di DEBUG \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="81dca-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="81dca-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="81dca-148">Questi flag determinano quali metodi [ADSI](active-directory-service-interfaces-adsi.md) verranno tracciati, in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="81dca-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81dca-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="81dca-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="81dca-150">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="81dca-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="81dca-151">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="81dca-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="81dca-152">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="81dca-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="81dca-153">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="81dca-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="81dca-154">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="81dca-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="81dca-155">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="81dca-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="81dca-156">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="81dca-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="81dca-157">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="81dca-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="81dca-158">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="81dca-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="81dca-159">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="81dca-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="81dca-160">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="81dca-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="81dca-161">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="81dca-161">DirectoryString</span></span></li>
<li><span data-ttu-id="81dca-162">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="81dca-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="81dca-163">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="81dca-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81dca-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="81dca-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="81dca-165">CADsUser:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="81dca-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81dca-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="81dca-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="81dca-167">CADsUser:: password</span><span class="sxs-lookup"><span data-stu-id="81dca-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81dca-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="81dca-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="81dca-169">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="81dca-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="81dca-170">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="81dca-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="81dca-171">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="81dca-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="81dca-172">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="81dca-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="81dca-173">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="81dca-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="81dca-174">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="81dca-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="81dca-175">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="81dca-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="81dca-176">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="81dca-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="81dca-177">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="81dca-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="81dca-178">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="81dca-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="81dca-179">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="81dca-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="81dca-180">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="81dca-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="81dca-181">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="81dca-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="81dca-182">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="81dca-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="81dca-183">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="81dca-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="81dca-184">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="81dca-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="81dca-185">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="81dca-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="81dca-186">È possibile combinare i flag combinando i bit appropriati nell'argomento *flag* .</span><span class="sxs-lookup"><span data-stu-id="81dca-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="81dca-187">Ad esempio, per specificare i flag **debug \_ schema** e **debug \_ BINDCACHE** , il valore *flag* appropriato sarà 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="81dca-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="81dca-188">Infine, il flag *TraceLevel* deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="81dca-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="81dca-189">**\_errore a livello di traccia \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="81dca-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="81dca-190">0x00000002</span></span><br/> |
| <span data-ttu-id="81dca-191">**\_informazioni sul livello di traccia \_**</span><span class="sxs-lookup"><span data-stu-id="81dca-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="81dca-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="81dca-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="81dca-193">**Traccia \_ Le \_ informazioni sul livello** determinano la registrazione di tutti gli eventi da parte del processo di traccia, mentre l' **errore a \_ livello \_ di traccia** causa la registrazione solo degli eventi di errore.</span><span class="sxs-lookup"><span data-stu-id="81dca-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="81dca-194">Per terminare la traccia, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="81dca-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="81dca-195">**tracelog.exe-stop** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="81dca-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="81dca-196">Nell'esempio precedente, *sessionname* ha lo stesso nome di quello fornito con il comando che ha avviato la sezione di traccia.</span><span class="sxs-lookup"><span data-stu-id="81dca-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="81dca-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="81dca-197">Remarks</span></span>

<span data-ttu-id="81dca-198">È più efficace tracciare solo processi specifici specificando un determinato PID anziché tracciare tutti i processi in un computer.</span><span class="sxs-lookup"><span data-stu-id="81dca-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="81dca-199">Se è necessario tracciare più applicazioni nello stesso computer, è possibile che si verifichi un effetto sulle prestazioni. è presente un output di debug sostanziale nelle sezioni orientate alle prestazioni del codice.</span><span class="sxs-lookup"><span data-stu-id="81dca-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="81dca-200">Inoltre, gli amministratori devono prestare attenzione a impostare correttamente le autorizzazioni dei file di log durante la traccia di più processi. in caso contrario, qualsiasi utente potrebbe essere in grado di leggere i log di traccia e altri utenti saranno in grado di tracciare processi che contengono informazioni protette.</span><span class="sxs-lookup"><span data-stu-id="81dca-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="81dca-201">Si supponga, ad esempio, che l'amministratore imposti la traccia per un'applicazione "Test.exe" e non specifichi un PID nel registro di sistema per tracciare più istanze del processo.</span><span class="sxs-lookup"><span data-stu-id="81dca-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="81dca-202">Un altro utente desidera quindi tracciare l'applicazione "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="81dca-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="81dca-203">Se i file di log di traccia non sono limitati correttamente, è necessario che l'utente rinomi "Secure.exe" in "Test.exe" e verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="81dca-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="81dca-204">In generale, è consigliabile tracciare solo processi specifici durante la risoluzione dei problemi e rimuovere la chiave del registro di sistema di traccia non appena viene eseguita la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="81dca-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="81dca-205">Poiché l'abilitazione della traccia eventi produrrà file di log aggiuntivi, gli amministratori dovrebbero monitorare attentamente le dimensioni dei file di registro; la mancanza di spazio su disco nel computer locale può causare un attacco Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="81dca-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="81dca-206">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="81dca-206">Example Scenarios</span></span>

<span data-ttu-id="81dca-207">Scenario 1: l'amministratore rileva un errore imprevisto in un'applicazione che imposta le password per gli account utente, in modo da eseguire la procedura seguente per risolvere il problema utilizzando la traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="81dca-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="81dca-208">Scrivere uno script per riprodurre il problema e creare la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="81dca-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="81dca-209">**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="81dca-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="81dca-210">Avviare una sessione di traccia, impostando *flag* su 0x2 (**debug \_ CHANGEPASSWD**) e *TraceLevel* su 0x4 (**\_ \_ informazioni sul livello di traccia**), usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="81dca-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="81dca-211">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-flag 0x4 a livello di 0x2**</span><span class="sxs-lookup"><span data-stu-id="81dca-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="81dca-212">Eseguire cscript.exe con lo script di test per riprodurre il problema e quindi terminare la sessione di traccia:</span><span class="sxs-lookup"><span data-stu-id="81dca-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="81dca-213">**tracelog.exe arrestare scripttrace**</span><span class="sxs-lookup"><span data-stu-id="81dca-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="81dca-214">Elimina la chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="81dca-214">Delete the registry key</span></span>

    <span data-ttu-id="81dca-215">**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="81dca-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="81dca-216">Eseguire lo strumento ETW Tracerpt.exe per analizzare le informazioni di traccia dal log:</span><span class="sxs-lookup"><span data-stu-id="81dca-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="81dca-217">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-flag 0x4 a livello di 0x2**</span><span class="sxs-lookup"><span data-stu-id="81dca-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="81dca-218">Scenario 2: l'amministratore desidera tracciare le operazioni di analisi e download dello schema in un'applicazione [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominata w3wp.exe già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81dca-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="81dca-219">A tale scopo, l'amministratore deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="81dca-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="81dca-220">Creazione della chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="81dca-220">Create the registry key</span></span>

    <span data-ttu-id="81dca-221">**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="81dca-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="81dca-222">all'interno di tale chiave, creare un valore di tipo DWORD denominato PID e impostarlo sull'ID processo dell'istanza di w3wp.exe attualmente in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="81dca-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="81dca-223">Viene quindi creata una sessione di traccia, impostando *flag* su 0x1 (**\_ schema di debug**) e *TraceLevel* su 0x4 (**\_ \_ informazioni sul livello di traccia**):</span><span class="sxs-lookup"><span data-stu-id="81dca-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="81dca-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ w3wp. etl-flag 0x4 a livello di 0x1**</span><span class="sxs-lookup"><span data-stu-id="81dca-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="81dca-225">Riprodurre l'operazione che richiede la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="81dca-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="81dca-226">Terminare la sessione di traccia:</span><span class="sxs-lookup"><span data-stu-id="81dca-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="81dca-227">**tracelog.exe arrestare w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="81dca-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="81dca-228">Eliminare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="81dca-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="81dca-229">Eseguire lo strumento ETW tracerpt.exe per analizzare le informazioni di traccia dal log:</span><span class="sxs-lookup"><span data-stu-id="81dca-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="81dca-230">**tracerpt.exe. \\ w3wp. etl-o-report**</span><span class="sxs-lookup"><span data-stu-id="81dca-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

