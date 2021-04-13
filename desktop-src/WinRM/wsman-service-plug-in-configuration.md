---
title: Configurazione del plug-in del servizio WinRM
description: Un plug-in di Gestione remota Windows (WinRM) deve essere registrato nel catalogo WinRM per consentire all'infrastruttura di determinare in modo dinamico il set di plug-in disponibili e gli URI delle risorse supportati.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339603"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="772fb-103">Configurazione del plug-in del servizio WinRM</span><span class="sxs-lookup"><span data-stu-id="772fb-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="772fb-104">Un plug-in di Gestione remota Windows (WinRM) deve essere registrato nel catalogo WinRM per consentire all'infrastruttura di determinare in modo dinamico il set di plug-in disponibili e gli [*URI delle risorse*](windows-remote-management-glossary.md) supportati.</span><span class="sxs-lookup"><span data-stu-id="772fb-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="772fb-105">Tutti gli [*URI di risorsa*](windows-remote-management-glossary.md) per i plug-in WinRM devono essere conformi al formato definito in RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ).</span><span class="sxs-lookup"><span data-stu-id="772fb-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="772fb-106">La configurazione viene eseguita tramite il servizio WinRM principale.</span><span class="sxs-lookup"><span data-stu-id="772fb-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="772fb-107">Il comando seguente registra una configurazione del plug-in con il servizio WinRM:</span><span class="sxs-lookup"><span data-stu-id="772fb-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="772fb-108">Il servizio gestione remota Windows deve essere riavviato per esporre i plug-in appena registrati.</span><span class="sxs-lookup"><span data-stu-id="772fb-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="772fb-109">La configurazione del plug-in è specificata in XML.</span><span class="sxs-lookup"><span data-stu-id="772fb-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="772fb-110">Di seguito è riportato un esempio.</span><span class="sxs-lookup"><span data-stu-id="772fb-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="772fb-111">Nell'elenco seguente vengono descritti in modo più dettagliato gli elementi XML ed è seguito dallo schema di configurazione specificato come XSD.</span><span class="sxs-lookup"><span data-stu-id="772fb-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="772fb-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**</span><span class="sxs-lookup"><span data-stu-id="772fb-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-113">Specifica il nome del file del plug-in per le operazioni.</span><span class="sxs-lookup"><span data-stu-id="772fb-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="772fb-114">Tutte le variabili di ambiente inserite in questa voce verranno espanse nel contesto degli utenti quando viene ricevuta una richiesta.</span><span class="sxs-lookup"><span data-stu-id="772fb-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="772fb-115">Ogni utente potrebbe avere una versione diversa della stessa variabile di ambiente, quindi ogni utente potrebbe finire con un plug-in diverso.</span><span class="sxs-lookup"><span data-stu-id="772fb-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="772fb-116">Questa voce non può essere vuota e deve puntare a un plug-in valido.</span><span class="sxs-lookup"><span data-stu-id="772fb-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nome**</span><span class="sxs-lookup"><span data-stu-id="772fb-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-118">Specifica il nome visualizzato da usare per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="772fb-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="772fb-119">Se dal plug-in viene restituito un errore, questo nome verrà inserito nel codice XML dell'errore restituito all'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="772fb-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="772fb-120">Il nome non è specifico delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="772fb-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Architettura** di</span><span class="sxs-lookup"><span data-stu-id="772fb-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-122">Specifica se il plug-in per le operazioni è a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="772fb-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="772fb-123">Se questo elemento non viene specificato, il valore predefinito sarà "32" nei sistemi x86 e "64" nei sistemi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="772fb-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="772fb-124">Per i sistemi x86, l'unico valore valido è "32".</span><span class="sxs-lookup"><span data-stu-id="772fb-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="772fb-125">Se il valore è "32" in un sistema a 64 bit, è necessario prendere in considerazione il reindirizzamento WOW64 quando si immettono le informazioni sul **nome del file** .</span><span class="sxs-lookup"><span data-stu-id="772fb-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="772fb-126">Il file system sottostante userà il reindirizzamento WOW64 per tradurre system32 in SysWow64.</span><span class="sxs-lookup"><span data-stu-id="772fb-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="772fb-127">Se, ad esempio, **filename** è "% windir% \\ system32 \\myplugin.dll" e **Architecture** è "32", il file del plug-in effettivo si trova in "% windir% \\ SysWow64 \\myplugin.dll".</span><span class="sxs-lookup"><span data-stu-id="772fb-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="772fb-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **XmlRenderingType**</span><span class="sxs-lookup"><span data-stu-id="772fb-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-129">Configura il formato in cui XML viene passato ai plug-in tramite l'oggetto [**\_ dati WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) .</span><span class="sxs-lookup"><span data-stu-id="772fb-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="772fb-130">Sono disponibili i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="772fb-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="772fb-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Testo</span><span class="sxs-lookup"><span data-stu-id="772fb-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="772fb-132">I dati XML in arrivo sono contenuti in una \_ \_ struttura di testo del tipo di dati WSMan \_ , che rappresenta l'XML come buffer di memoria **PCWSTR** .</span><span class="sxs-lookup"><span data-stu-id="772fb-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span><span class="sxs-lookup"><span data-stu-id="772fb-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="772fb-134">I dati XML in arrivo sono contenuti in un \_ tipo di dati WSMan \_ \_ \_ \_ struttura del Reader WS XML, che rappresenta l'XML come oggetto **XmlReader** , definito nel file di intestazione WebServices. h.</span><span class="sxs-lookup"><span data-stu-id="772fb-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="772fb-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**</span><span class="sxs-lookup"><span data-stu-id="772fb-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-136">Questo nodo è facoltativo e consente a un plug-in di configurare codice XML aggiuntivo che verrà passato al metodo [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).</span><span class="sxs-lookup"><span data-stu-id="772fb-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="772fb-137">Questa informazione aggiuntiva non è necessaria per la maggior parte dei plug-in, ma se è necessario usare un plug-in in più scenari che richiedono una semantica di runtime diversa, questo codice XML fornirà la flessibilità necessaria per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="772fb-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Risorse** di</span><span class="sxs-lookup"><span data-stu-id="772fb-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-139">Specifica un elenco di [*URI di risorsa*](windows-remote-management-glossary.md)supportati da questo plug-in.</span><span class="sxs-lookup"><span data-stu-id="772fb-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="772fb-140">È necessario specificare almeno una voce **resourceUri**. in caso contrario, il codice XML verrà rifiutato.</span><span class="sxs-lookup"><span data-stu-id="772fb-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** di</span><span class="sxs-lookup"><span data-stu-id="772fb-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-142">Rappresenta una singola configurazione [*URI di risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="772fb-143">L'attributo **SupportsOptions** può essere impostato su false.</span><span class="sxs-lookup"><span data-stu-id="772fb-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="772fb-144">Se **SupportsOptions** è impostato su false, questo attributo non viene elencato quando la risorsa viene enumerata.</span><span class="sxs-lookup"><span data-stu-id="772fb-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="772fb-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **ResourceUri**</span><span class="sxs-lookup"><span data-stu-id="772fb-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-146">Specifica un singolo [*URI di risorsa*](windows-remote-management-glossary.md) in formato completo o come stringa di corrispondenza parziale basata sull'attributo **exactMatch** .</span><span class="sxs-lookup"><span data-stu-id="772fb-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="772fb-147">Se **exactMatch** non è presente, il valore predefinito è **false**, il che significa che il processore SOAP WinRM eseguirà una corrispondenza parziale all'inizio dell' *URI della risorsa* e, in caso di corrispondenza, lo passerà al plug-in.</span><span class="sxs-lookup"><span data-stu-id="772fb-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="772fb-148">È possibile specificare l'attributo **SupportsOptions** se all' *URI della risorsa* è consentito passare qualsiasi opzione.</span><span class="sxs-lookup"><span data-stu-id="772fb-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="772fb-149">Per impostazione predefinita, non sono supportate opzioni e, se presenti nella richiesta client, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="772fb-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="772fb-150">Se le opzioni sono supportate dal plug-in, è importante che il plug-in restituisca l'errore corretto se è presente un'opzione che il plug-in non riconosce quando il flag **MustUnderstand** è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="772fb-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **Funzionalità** di</span><span class="sxs-lookup"><span data-stu-id="772fb-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-152">Specifica una funzionalità disponibile in questo URI di [*risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-153">Sarà presente una voce per ogni tipo di operazione supportata.</span><span class="sxs-lookup"><span data-stu-id="772fb-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="772fb-154">Sono disponibili le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="772fb-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="772fb-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Ottieni</span><span class="sxs-lookup"><span data-stu-id="772fb-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="772fb-156">Le operazioni get sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-157">L'attributo **SupportFragment** viene usato se l'operazione Get supporta il concetto.</span><span class="sxs-lookup"><span data-stu-id="772fb-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="772fb-158">L'attributo **SupportFiltering** non è valido e deve essere impostato su false.</span><span class="sxs-lookup"><span data-stu-id="772fb-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="772fb-159">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Mettere</span><span class="sxs-lookup"><span data-stu-id="772fb-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="772fb-161">Le operazioni Put sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-162">L'attributo **SupportFragment** viene usato se l'operazione Put supporta il concetto.</span><span class="sxs-lookup"><span data-stu-id="772fb-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="772fb-163">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-164">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Creare</span><span class="sxs-lookup"><span data-stu-id="772fb-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="772fb-166">Le operazioni di creazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-167">L'attributo **SupportFragment** viene usato se l'operazione Create supporta il concetto.</span><span class="sxs-lookup"><span data-stu-id="772fb-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="772fb-168">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-169">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Eliminare</span><span class="sxs-lookup"><span data-stu-id="772fb-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="772fb-171">Le operazioni di eliminazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-172">L'attributo **SupportFragment** viene usato se l'operazione Delete supporta il concetto.</span><span class="sxs-lookup"><span data-stu-id="772fb-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="772fb-173">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-174">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Richiamare</span><span class="sxs-lookup"><span data-stu-id="772fb-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="772fb-176">Le operazioni Invoke sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-177">L'attributo **SupportFragment** non è supportato per le operazioni Invoke e deve essere impostato su false.</span><span class="sxs-lookup"><span data-stu-id="772fb-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="772fb-178">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-179">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerare</span><span class="sxs-lookup"><span data-stu-id="772fb-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="772fb-181">Le operazioni di enumerazione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-182">L'attributo **SupportFragment** non è supportato per le operazioni di enumerazione e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="772fb-183">L'attributo **SupportFiltering** è valido e se il plug-in supporta il filtro di questo attributo deve essere impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="772fb-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="772fb-184">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Sottoscrivere</span><span class="sxs-lookup"><span data-stu-id="772fb-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="772fb-186">Le operazioni di sottoscrizione sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-187">L'attributo **SupportFragment** non è supportato per le operazioni di sottoscrizione e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="772fb-188">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-189">Questa funzionalità non è valida per un *URI di risorsa* se sono supportate anche le operazioni della shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="772fb-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="772fb-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="772fb-191">Le operazioni della shell sono supportate nell' [*URI della risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="772fb-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="772fb-192">L'attributo **SupportFragment** non è supportato per le operazioni della shell e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="772fb-193">L'attributo **SupportFiltering** non è valido e deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="772fb-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="772fb-194">Questa funzionalità non è valida per un *URI di risorsa* se è supportata anche un'altra funzionalità dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="772fb-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="772fb-195">Se è configurata una funzionalità di operazione Shell per un *URI di risorsa*, le operazioni get, put, create, DELETE, Invoke ed enumerate vengono elaborate internamente nel servizio WinRM per gestire le shell.</span><span class="sxs-lookup"><span data-stu-id="772fb-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="772fb-196">Di conseguenza, il plug-in non è in grado di gestire le operazioni.</span><span class="sxs-lookup"><span data-stu-id="772fb-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="772fb-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Risorse** / di **Risorsa** / di **Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="772fb-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="772fb-198">Questo elemento definisce il descrittore di sicurezza (tramite l'attributo **SDDL** ) da applicare per determinare l'accesso a un [*URI di risorsa*](windows-remote-management-glossary.md) specifico (tramite l'attributo **URI** ).</span><span class="sxs-lookup"><span data-stu-id="772fb-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="772fb-199">Se **exactMatch** non è presente, l'impostazione predefinita dell'elemento di **sicurezza** è **false**, il che significa che **SDDL** si applica a tutti gli *URI di risorsa* che condividono **URI** come prefisso.</span><span class="sxs-lookup"><span data-stu-id="772fb-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="772fb-200">Se **exactMatch** è impostato su true, **SDDL** si applica solo all' **URI** esatto specificato.</span><span class="sxs-lookup"><span data-stu-id="772fb-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="772fb-201">Se sono presenti più voci di **sicurezza** che possono essere applicate a uno specifico *URI di risorsa*, viene usata la corrispondenza del prefisso più lungo per determinare l' **SDDL** appropriato.</span><span class="sxs-lookup"><span data-stu-id="772fb-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="772fb-202">In seguito alla corrispondenza del prefisso più lungo, se esiste una voce **URI** esatta della corrispondenza, viene sempre scelta come elemento di sicurezza appropriato.</span><span class="sxs-lookup"><span data-stu-id="772fb-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="772fb-203">Di seguito è riportato lo schema di configurazione del plug-in specificato come XSD.</span><span class="sxs-lookup"><span data-stu-id="772fb-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




