---
title: Tipo complesso ChannelType
description: Definisce un canale al quale i provider possono registrare gli eventi.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- Log eventi di tipo complesso ChannelType
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478143"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="b9a7d-104">Tipo complesso ChannelType</span><span class="sxs-lookup"><span data-stu-id="b9a7d-104">ChannelType Complex Type</span></span>

<span data-ttu-id="b9a7d-105">Definisce un canale al quale i provider possono registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-105">Defines a channel to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b9a7d-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b9a7d-106">Child elements</span></span>



| <span data-ttu-id="b9a7d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9a7d-107">Element</span></span>                                                                  | <span data-ttu-id="b9a7d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-108">Type</span></span>                                                                                   | <span data-ttu-id="b9a7d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9a7d-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9a7d-110">**registrazione**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="b9a7d-111">**ChannelLoggingType**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="b9a7d-112">Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se il file di log è sequenziale o circolare.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="b9a7d-113">**editrice**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="b9a7d-114">**ChannelPublishingType**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="b9a7d-115">Definisce le proprietà di registrazione per la sessione utilizzata dal canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="b9a7d-116">Solo i canali di debug e analitici e i canali che utilizzano l'isolamento personalizzato possono specificare le proprietà di registrazione per la sessione.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b9a7d-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="b9a7d-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9a7d-118">Nome</span><span class="sxs-lookup"><span data-stu-id="b9a7d-118">Name</span></span></th>
<th><span data-ttu-id="b9a7d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-119">Type</span></span></th>
<th><span data-ttu-id="b9a7d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9a7d-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9a7d-121">access</span><span class="sxs-lookup"><span data-stu-id="b9a7d-121">access</span></span></td>
<td><span data-ttu-id="b9a7d-122">string</span><span class="sxs-lookup"><span data-stu-id="b9a7d-122">string</span></span></td>
<td><span data-ttu-id="b9a7d-123">Descrittore di accesso SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ) che controlla l'accesso al file di log che esegue il backup del canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="b9a7d-124">Se l'attributo <strong>Isolation</strong> è impostato su Application o System, il descrittore di accesso controlla l'accesso in lettura al file (le autorizzazioni di scrittura vengono ignorate).</span><span class="sxs-lookup"><span data-stu-id="b9a7d-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="b9a7d-125">Se l'attributo <strong>Isolation</strong> è impostato su Custom, il descrittore di accesso controlla l'accesso in scrittura al canale e l'accesso in lettura al file.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9a7d-126">figlio</span><span class="sxs-lookup"><span data-stu-id="b9a7d-126">chid</span></span></td>
<td><span data-ttu-id="b9a7d-127">token</span><span class="sxs-lookup"><span data-stu-id="b9a7d-127">token</span></span></td>
<td><span data-ttu-id="b9a7d-128">Identificatore che identifica in modo univoco il canale nell'elenco di canali che il provider definisce o importa.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="b9a7d-129">Utilizzare questo valore quando si fa riferimento al canale in un evento.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="b9a7d-130">Se non si specifica un identificatore di canale, utilizzare il nome del canale per fare riferimento a questo canale in una definizione di evento.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9a7d-131">Enabled</span><span class="sxs-lookup"><span data-stu-id="b9a7d-131">enabled</span></span></td>
<td><span data-ttu-id="b9a7d-132">boolean</span><span class="sxs-lookup"><span data-stu-id="b9a7d-132">boolean</span></span></td>
<td><span data-ttu-id="b9a7d-133">Determina se il canale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="b9a7d-134">Impostare su <strong>true</strong> per consentire la registrazione sul canale. in caso contrario, <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="b9a7d-135">Il valore predefinito è <strong>false</strong> (la registrazione è disabilitata).</span><span class="sxs-lookup"><span data-stu-id="b9a7d-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="b9a7d-136">Poiché i tipi di canale di debug e analitico sono canali di volumi elevati, è necessario abilitare il canale solo quando si esamina un problema relativo a un componente che scrive su tale canale. in caso contrario, il canale rimarrà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="b9a7d-137">Ogni volta che si Abilita un canale di debug e analitico, il servizio Cancella gli eventi dal canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9a7d-138">Isolamento</span><span class="sxs-lookup"><span data-stu-id="b9a7d-138">isolation</span></span></td>
<td><span data-ttu-id="b9a7d-139">string</span><span class="sxs-lookup"><span data-stu-id="b9a7d-139">string</span></span></td>
<td><span data-ttu-id="b9a7d-140">Il valore di isolamento definisce le autorizzazioni di accesso predefinite per il canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="b9a7d-141">È possibile specificare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9a7d-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b9a7d-142"><strong>Applicazione</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="b9a7d-143"><strong>Sistema</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="b9a7d-144"><strong>Impostazione personalizzata</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="b9a7d-145">L'isolamento predefinito è <strong>Application</strong>.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="b9a7d-146">Le autorizzazioni predefinite per l' <strong>applicazione</strong> sono (visualizzate con SDDL):</span><span class="sxs-lookup"><span data-stu-id="b9a7d-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9a7d-147">Testo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-147">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="b9a7d-148">Le autorizzazioni predefinite per il <strong>sistema</strong> sono (visualizzate con SDDL):</span><span class="sxs-lookup"><span data-stu-id="b9a7d-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9a7d-149">Testo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-149">Text</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b9a7d-150">Le autorizzazioni predefinite per l'isolamento <strong>personalizzato</strong> sono identiche a quelle dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="b9a7d-151">I canali che specificano l'isolamento <strong>dell'applicazione</strong> utilizzano la stessa sessione ETW.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="b9a7d-152">Lo stesso vale per l'isolamento del <strong>sistema</strong> .</span><span class="sxs-lookup"><span data-stu-id="b9a7d-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="b9a7d-153">Tuttavia, se si specifica un isolamento <strong>personalizzato</strong> , il servizio crea una sessione ETW separata per il canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="b9a7d-154">L'uso dell'isolamento <strong>personalizzato</strong> consente di controllare le autorizzazioni di accesso per il canale e il file di backup.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="b9a7d-155">Poiché sono disponibili solo 64 sessioni ETW, è consigliabile limitare l'utilizzo dell'isolamento <strong>personalizzato</strong> .</span><span class="sxs-lookup"><span data-stu-id="b9a7d-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9a7d-156">message</span><span class="sxs-lookup"><span data-stu-id="b9a7d-156">message</span></span></td>
<td><span data-ttu-id="b9a7d-157">string</span><span class="sxs-lookup"><span data-stu-id="b9a7d-157">string</span></span></td>
<td><p><span data-ttu-id="b9a7d-158">Nome visualizzato localizzato per il canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-158">The localized display name for the channel.</span></span> <span data-ttu-id="b9a7d-159">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione <a href="eventmanifestschema-stringtable-resources-element.md"><strong>un'STRINGTABLE</strong></a> del manifesto.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9a7d-160">name</span><span class="sxs-lookup"><span data-stu-id="b9a7d-160">name</span></span></td>
<td><span data-ttu-id="b9a7d-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="b9a7d-161">anyURI</span></span></td>
<td><p><span data-ttu-id="b9a7d-162">Nome del canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-162">The name of the channel.</span></span> <span data-ttu-id="b9a7d-163">Il nome deve essere univoco all'interno dell'elenco di canali utilizzati dal provider.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="b9a7d-164">La convenzione per la denominazione dei canali consiste nell'accodare il tipo di canale al nome del provider.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="b9a7d-165">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="b9a7d-165">For example.</span></span> <span data-ttu-id="b9a7d-166">Se il nome del provider è società-prodotto-componente e si sta definendo un canale operativo, il nome sarà società-prodotto-componente/operativo.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="b9a7d-167">I nomi di canale devono essere inferiori a 255 caratteri e non possono contenere i caratteri seguenti:' >','</span><span class="sxs-lookup"><span data-stu-id="b9a7d-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9a7d-168">simbolo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-168">symbol</span></span></td>
<td><span data-ttu-id="b9a7d-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9a7d-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="b9a7d-170">Simbolo da utilizzare per fare riferimento al canale nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="b9a7d-171">Il <a href="message-compiler--mc-exe-.md"><strong>compilatore di messaggi (MC.exe)</strong></a> usa il simbolo per creare una costante per il canale nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="b9a7d-172">Se non si specifica un simbolo, il compilatore genera automaticamente il nome.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b9a7d-173">tipo</span><span class="sxs-lookup"><span data-stu-id="b9a7d-173">type</span></span></td>
<td><span data-ttu-id="b9a7d-174">string</span><span class="sxs-lookup"><span data-stu-id="b9a7d-174">string</span></span></td>
<td><p><span data-ttu-id="b9a7d-175">Identifica il tipo del canale.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-175">Identifies the channel's type.</span></span> <span data-ttu-id="b9a7d-176">È possibile specificare uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9a7d-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="b9a7d-177"><strong>Admin</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="b9a7d-178"><strong>Operativo</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="b9a7d-179"><strong>Analitici</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="b9a7d-180"><strong>Eseguire il debug</strong></span><span class="sxs-lookup"><span data-stu-id="b9a7d-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="b9a7d-181">I canali di tipo amministratore supportano gli eventi destinati agli utenti finali, agli amministratori e al personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="b9a7d-182">Gli eventi scritti nei canali di amministrazione devono disporre di una soluzione ben definita su cui l'amministratore può agire. Un esempio di evento di amministrazione è un evento che si verifica quando un'applicazione non riesce a connettersi a una stampante.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="b9a7d-183">Questi eventi sono ben documentati o hanno un messaggio associato che fornisce al lettore istruzioni dirette sulle operazioni da eseguire per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="b9a7d-184">I canali dei tipi operativi supportano gli eventi utilizzati per l'analisi e la diagnosi di un problema o di un'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="b9a7d-185">Si possono utilizzare per lanciare strumenti o attività basati sul problema o sull'occorrenza.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="b9a7d-186">Un esempio di un evento operativo è un evento che si verifica quando si aggiunge o rimuove una stampante da un sistema.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="b9a7d-187">I canali di tipo analitico supportano gli eventi pubblicati in volume elevato.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="b9a7d-188">Essi descrivono le operazioni del programma e indicano problemi che non possono essere gestiti dall'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="b9a7d-189">I canali del tipo di debug supportano gli eventi utilizzati esclusivamente dagli sviluppatori per diagnosticare un problema per il debug.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="b9a7d-190">I canali analitici e di debug sono disabilitati per impostazione predefinita e devono essere abilitati solo per determinare la causa di un problema.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="b9a7d-191">Ad esempio, è possibile abilitare il canale, eseguire lo scenario che causa il problema, disabilitare il canale e quindi eseguire una query sugli eventi.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="b9a7d-192">Si noti che l'abilitazione del canale cancella il canale degli eventi esistenti.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="b9a7d-193">Se il canale analitico e di debug utilizza un file di supporto circolare, è necessario disabilitare il canale per eseguire una query sui relativi eventi.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="b9a7d-194">Tutti i canali amministrativi utilizzano la stessa sessione ETW; lo stesso vale per i canali operativi.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="b9a7d-195">Tuttavia, ogni canale analitico e di debug utilizza una sessione ETW separata, che è un altro motivo per abilitare questi tipi di canale solo quando necessario (è disponibile un numero limitato di sessioni ETW).</span><span class="sxs-lookup"><span data-stu-id="b9a7d-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b9a7d-196">Valore</span><span class="sxs-lookup"><span data-stu-id="b9a7d-196">value</span></span></td>
<td><span data-ttu-id="b9a7d-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9a7d-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="b9a7d-198">Identificatore numerico che identifica in modo univoco il canale nell'elenco dei canali definiti dal provider.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="b9a7d-199">Il compilatore di messaggi assegna il valore se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b9a7d-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9a7d-200">Remarks</span></span>

<span data-ttu-id="b9a7d-201">Se il nome del canale segue la convenzione di denominazione del canale, il Visualizzatore eventi di Windows elenca il canale usando la stringa che segue la barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="b9a7d-202">Se, ad esempio, il nome del canale è azienda-prodotto-componente/operativo, il Visualizzatore eventi elenca il canale come operativo nel provider del componente società-prodotto.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="b9a7d-203">In caso contrario, il nome dell'intero canale viene visualizzato nel provider.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="b9a7d-204">Se specificato, viene usato il nome visualizzato localizzato.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a7d-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9a7d-205">Requirements</span></span>



| <span data-ttu-id="b9a7d-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a7d-206">Requirement</span></span> | <span data-ttu-id="b9a7d-207">Valore</span><span class="sxs-lookup"><span data-stu-id="b9a7d-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9a7d-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a7d-208">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a7d-209">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9a7d-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9a7d-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a7d-210">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a7d-211">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9a7d-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
