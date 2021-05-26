---
title: Traccia eventi in ADSI
description: Windows Server 2008 e Windows Vista introducono Event Tracing in Active Directory Service Interfaces (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- event tracing ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423712"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="cce65-104">Traccia eventi in ADSI</span><span class="sxs-lookup"><span data-stu-id="cce65-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="cce65-105">Windows Server 2008 e Windows Vista introducono [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in Active Directory [Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="cce65-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="cce65-106">Alcune aree del provider LDAP ADSI hanno un'implementazione sottostante complessa o che prevede una sequenza di passaggi che rende difficile la diagnosi dei problemi.</span><span class="sxs-lookup"><span data-stu-id="cce65-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="cce65-107">Per consentire agli sviluppatori di applicazioni di risolvere i problemi, Event Tracing è stato aggiunto alle aree seguenti:</span><span class="sxs-lookup"><span data-stu-id="cce65-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="cce65-108">Analisi e download dello schema</span><span class="sxs-lookup"><span data-stu-id="cce65-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="cce65-109">L'interfaccia IADs in ADSI richiede che lo schema LDAP venga memorizzato nella cache del client in modo che sia possibile effettuare correttamente il marshalling degli attributi (come descritto nel modello [di schema ADSI).](adsi-schema-model.md)</span><span class="sxs-lookup"><span data-stu-id="cce65-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="cce65-110">A tale scopo, ADSI carica lo schema per ogni processo (e per ogni server/dominio LDAP) in memoria da un file di schema (con estensione sch) salvato sul disco locale o scaricarlo dal server LDAP.</span><span class="sxs-lookup"><span data-stu-id="cce65-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="cce65-111">Processi diversi nello stesso computer client usano lo schema memorizzato nella cache su disco, se disponibile e applicabile.</span><span class="sxs-lookup"><span data-stu-id="cce65-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="cce65-112">Se non è possibile ottenere lo schema dal disco o dal server, ADSI usa uno schema predefinito hardcoded.</span><span class="sxs-lookup"><span data-stu-id="cce65-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="cce65-113">In questo caso, non è possibile effettuare il marshalling degli attributi che non fanno parte di questo schema predefinito e ADSI restituisce un errore durante il recupero di questi attributi.</span><span class="sxs-lookup"><span data-stu-id="cce65-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="cce65-114">Questo problema può essere causato da diversi fattori, tra cui problemi di analisi dello schema e privilegi insufficienti per scaricare lo schema.</span><span class="sxs-lookup"><span data-stu-id="cce65-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="cce65-115">Spesso è difficile determinare il motivo per cui viene usato un determinato schema predefinito.</span><span class="sxs-lookup"><span data-stu-id="cce65-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="cce65-116">L'uso di Traccia eventi in quest'area consente di diagnosticare più rapidamente il problema e risolverlo.</span><span class="sxs-lookup"><span data-stu-id="cce65-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="cce65-117">Modifica e impostazione della password</span><span class="sxs-lookup"><span data-stu-id="cce65-117">Changing and Setting the Password</span></span>

<span data-ttu-id="cce65-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) utilizzano più meccanismi per eseguire l'operazione richiesta in base alla configurazione disponibile( come descritto in Impostazione e modifica delle password utente con [il provider LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="cce65-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="cce65-119">Quando **ChangePassword** e **SetPassword** hanno esito negativo, può essere difficile determinare esattamente il motivo e Traccia eventi consente di risolvere i problemi con questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cce65-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="cce65-120">Cache di binding ADSI</span><span class="sxs-lookup"><span data-stu-id="cce65-120">ADSI Bind Cache</span></span>

<span data-ttu-id="cce65-121">ADSI tenta internamente di riutilizzare le connessioni LDAP quando possibile (vedere [Memorizzazione nella cache delle connessioni](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="cce65-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="cce65-122">Durante la risoluzione dei problemi, è utile verificare se è stata aperta una nuova connessione per la comunicazione con il server o se è stata usata una connessione esistente.</span><span class="sxs-lookup"><span data-stu-id="cce65-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="cce65-123">Può anche essere utile tracciare il ciclo di vita della cache di connessione (talvolta definita cache di binding) e la relativa creazione o chiusura e se è stata verificata una segnalazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="cce65-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="cce65-124">Nel caso di un binding [serverless,](/windows/desktop/AD/serverless-binding-and-rootdse)ADSI chiama il localizzatore DC per selezionare un server per il dominio del contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cce65-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="cce65-125">ADSI gestisce quindi una cache del mapping dominio-server per le connessioni successive.</span><span class="sxs-lookup"><span data-stu-id="cce65-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="cce65-126">Traccia eventi consente di tracciare la selezione del controller di dominio ed è quindi utile per la risoluzione dei problemi relativi alla connessione.</span><span class="sxs-lookup"><span data-stu-id="cce65-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="cce65-127">Abilitazione della traccia e avvio di una sessione di traccia</span><span class="sxs-lookup"><span data-stu-id="cce65-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="cce65-128">Per attivare la traccia ADSI, creare la chiave del Registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="cce65-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="cce65-129">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**</span><span class="sxs-lookup"><span data-stu-id="cce65-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="cce65-130">*ProcessName* è il nome completo del processo che si vuole tracciare, inclusa l'estensione (ad esempio, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="cce65-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="cce65-131">È anche possibile inserire un valore facoltativo di tipo **DWORD** denominato PID in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="cce65-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="cce65-132">È consigliabile impostare questo valore e quindi tracciare solo un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="cce65-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="cce65-133">In caso contrario, verranno tracciate tutte le istanze dell'applicazione specificate da *ProcessName.*</span><span class="sxs-lookup"><span data-stu-id="cce65-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="cce65-134">Eseguire quindi il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="cce65-134">Then execute the following command:</span></span>

<span data-ttu-id="cce65-135">**tracelog.exe -start** *sessionname* **-guid \#** provider _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span><span class="sxs-lookup"><span data-stu-id="cce65-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="cce65-136">*sessionname* è semplicemente un identificatore arbitrario usato per etichettare la sessione di traccia. Sarà necessario fare riferimento a questo nome di sessione in un secondo momento quando si arresta la sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="cce65-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="cce65-137">Il GUID per il provider di rilevamento ADSI è "7288c9f8-d63c-4932-a345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="cce65-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="cce65-138">*filename* specifica il file di log in cui verranno scritti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="cce65-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="cce65-139">*traceFlags* deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cce65-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="cce65-140">Flag</span><span class="sxs-lookup"><span data-stu-id="cce65-140">Flag</span></span>                        |         <span data-ttu-id="cce65-141">valore</span><span class="sxs-lookup"><span data-stu-id="cce65-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="cce65-142">**DEBUG \_ SCHEMA**</span><span class="sxs-lookup"><span data-stu-id="cce65-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="cce65-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cce65-143">0x00000001</span></span><br/> |
| <span data-ttu-id="cce65-144">**DEBUG \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="cce65-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="cce65-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cce65-145">0x00000002</span></span><br/> |
| <span data-ttu-id="cce65-146">**DEBUG \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="cce65-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="cce65-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cce65-147">0x00000004</span></span><br/> |
| <span data-ttu-id="cce65-148">**ESEGUIRE IL DEBUG \_ DI BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="cce65-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="cce65-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="cce65-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="cce65-150">Questi flag determinano [quali metodi ADSI](active-directory-service-interfaces-adsi.md) verranno tracciati, in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="cce65-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cce65-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="cce65-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="cce65-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="cce65-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="cce65-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="cce65-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="cce65-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="cce65-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="cce65-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="cce65-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="cce65-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="cce65-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="cce65-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="cce65-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="cce65-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="cce65-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="cce65-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="cce65-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="cce65-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="cce65-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="cce65-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="cce65-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="cce65-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="cce65-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="cce65-163">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="cce65-163">DirectoryString</span></span></li>
<li><span data-ttu-id="cce65-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="cce65-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="cce65-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="cce65-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce65-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="cce65-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="cce65-167">CADsUser::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="cce65-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cce65-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="cce65-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="cce65-169">CADsUser::SetPassword</span><span class="sxs-lookup"><span data-stu-id="cce65-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cce65-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="cce65-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="cce65-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="cce65-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="cce65-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="cce65-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="cce65-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="cce65-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="cce65-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="cce65-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="cce65-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="cce65-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="cce65-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="cce65-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="cce65-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="cce65-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="cce65-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="cce65-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="cce65-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="cce65-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="cce65-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="cce65-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="cce65-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="cce65-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="cce65-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="cce65-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="cce65-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="cce65-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="cce65-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="cce65-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="cce65-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="cce65-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="cce65-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="cce65-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="cce65-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="cce65-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cce65-188">È possibile combinare i flag combinando i bit appropriati *nell'argomento traceFlags.*</span><span class="sxs-lookup"><span data-stu-id="cce65-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="cce65-189">Ad esempio, per specificare i **flag DEBUG \_ SCHEMA** e **DEBUG \_ BINDCACHE,** il valore *traceFlags* appropriato sarà 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="cce65-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="cce65-190">Infine, il flag *traceLevel* deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cce65-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="cce65-191">Flag</span><span class="sxs-lookup"><span data-stu-id="cce65-191">Flag</span></span>                                    |       <span data-ttu-id="cce65-192">valore</span><span class="sxs-lookup"><span data-stu-id="cce65-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="cce65-193">**ERRORE A \_ LIVELLO \_ DI TRACCIA**</span><span class="sxs-lookup"><span data-stu-id="cce65-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="cce65-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cce65-194">0x00000002</span></span><br/> |
| <span data-ttu-id="cce65-195">**INFORMAZIONI SUL \_ LIVELLO \_ DI TRACCIA**</span><span class="sxs-lookup"><span data-stu-id="cce65-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="cce65-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cce65-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="cce65-197">**TRACE \_ LEVEL \_ INFORMATION fa** sì che il processo di traccia registri tutti gli eventi, mentre TRACE LEVEL **\_ \_ ERROR** fa sì che il processo di traccia registri solo gli eventi di errore.</span><span class="sxs-lookup"><span data-stu-id="cce65-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="cce65-198">Per terminare la traccia, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="cce65-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="cce65-199">**tracelog.exe -stop** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="cce65-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="cce65-200">Nell'esempio precedente *sessionname* è lo stesso nome di quello fornito con il comando che ha avviato la sezione di traccia.</span><span class="sxs-lookup"><span data-stu-id="cce65-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce65-201">Commenti</span><span class="sxs-lookup"><span data-stu-id="cce65-201">Remarks</span></span>

<span data-ttu-id="cce65-202">È più efficace tracciare solo processi specifici specificando un PID specifico anziché tracciare tutti i processi in un computer.</span><span class="sxs-lookup"><span data-stu-id="cce65-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="cce65-203">Se è necessario tracciare più applicazioni nello stesso computer, potrebbe verificarsi un impatto sulle prestazioni. È disponibile un output di debug sostanziale nelle sezioni del codice orientate alle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cce65-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="cce65-204">Inoltre, gli amministratori devono prestare attenzione a impostare correttamente le autorizzazioni dei file di log durante la traccia di più processi. In caso contrario, qualsiasi utente potrebbe essere in grado di leggere i log di traccia e altri utenti saranno in grado di tracciare i processi che contengono informazioni protette.</span><span class="sxs-lookup"><span data-stu-id="cce65-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="cce65-205">Si supponga, ad esempio, che l'amministratore configura la traccia per un'applicazione "Test.exe" e non specifica un PID nel Registro di sistema per tracciare più istanze del processo.</span><span class="sxs-lookup"><span data-stu-id="cce65-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="cce65-206">Un altro utente vuole ora tracciare l'applicazione "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="cce65-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="cce65-207">Se i file di log di traccia non sono limitati correttamente, l'utente deve solo rinominare "Secure.exe" in "Test.exe" e ne verrà tracciata la traccia.</span><span class="sxs-lookup"><span data-stu-id="cce65-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="cce65-208">In generale, è meglio tracciare solo processi specifici durante la risoluzione dei problemi e rimuovere la chiave del Registro di sistema di traccia non appena viene eseguita la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="cce65-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="cce65-209">Poiché l'abilitazione di Traccia eventi produrrà file di log aggiuntivi, gli amministratori devono monitorare attentamente le dimensioni dei file di log. La mancanza di spazio su disco nel computer locale può causare una negazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="cce65-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="cce65-210">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="cce65-210">Example Scenarios</span></span>

<span data-ttu-id="cce65-211">Scenario 1: l'amministratore rileva un errore imprevisto in un'applicazione che imposta le password per gli account utente, quindi deve seguire questa procedura per risolvere il problema usando Traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="cce65-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="cce65-212">Scrivere uno script che riproduci il problema e creare la chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="cce65-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="cce65-213">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="cce65-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="cce65-214">Avviare una sessione di traccia, impostando *traceFlags* su 0x2 (**DEBUG \_ CHANGEPASSWD**) e *traceLevel* su 0x4 (**TRACE LEVEL \_ \_ INFORMATION**), usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="cce65-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="cce65-215">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="cce65-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="cce65-216">Eseguire cscript.exe con lo script di test per riprodurre il problema e quindi terminare la sessione di traccia:</span><span class="sxs-lookup"><span data-stu-id="cce65-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="cce65-217">**tracelog.exe -stop scripttrace**</span><span class="sxs-lookup"><span data-stu-id="cce65-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="cce65-218">Eliminare la chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="cce65-218">Delete the registry key</span></span>

    <span data-ttu-id="cce65-219">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="cce65-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="cce65-220">Eseguire lo strumento ETW Tracerpt.exe analizzare le informazioni di traccia dal log:</span><span class="sxs-lookup"><span data-stu-id="cce65-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="cce65-221">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="cce65-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="cce65-222">Scenario 2: l'amministratore vuole tracciare le operazioni di analisi e download dello schema in un'applicazione [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominata w3wp.exe già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cce65-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="cce65-223">A tale scopo, l'amministratore deve seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="cce65-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="cce65-224">Creare la chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="cce65-224">Create the registry key</span></span>

    <span data-ttu-id="cce65-225">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="cce65-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="cce65-226">e all'interno di tale chiave, creare un valore di tipo DWORD denominato PID e impostarlo sull'ID processo dell'istanza di w3wp.exe attualmente in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="cce65-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="cce65-227">Creano quindi una sessione di traccia, impostando *traceFlags* su 0x1 (**DEBUG \_ SCHEMA**) e *traceLevel* su 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):</span><span class="sxs-lookup"><span data-stu-id="cce65-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="cce65-228">**tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="cce65-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="cce65-229">Riprodurre l'operazione che richiede la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="cce65-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="cce65-230">Terminare la sessione di traccia:</span><span class="sxs-lookup"><span data-stu-id="cce65-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="cce65-231">**tracelog.exe -stop w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="cce65-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="cce65-232">Eliminare la chiave del Registro di **sistema HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="cce65-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="cce65-233">Eseguire lo strumento ETW tracerpt.exe analizzare le informazioni di traccia dal log:</span><span class="sxs-lookup"><span data-stu-id="cce65-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="cce65-234">**tracerpt.exe . \\ w3wp.etl -o -report**</span><span class="sxs-lookup"><span data-stu-id="cce65-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

