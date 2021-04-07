---
title: Prefissi URI
description: Il prefisso dell'URI della risorsa è diverso a seconda del XML Schema che descrive la risorsa.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103873089"
---
# <a name="uri-prefixes"></a><span data-ttu-id="97033-103">Prefissi URI</span><span class="sxs-lookup"><span data-stu-id="97033-103">URI prefixes</span></span>

<span data-ttu-id="97033-104">Il prefisso dell' [*URI della risorsa*](windows-remote-management-glossary.md) è diverso a seconda del XML Schema che descrive la risorsa.</span><span class="sxs-lookup"><span data-stu-id="97033-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="97033-105">Prefissi</span><span class="sxs-lookup"><span data-stu-id="97033-105">Prefixes</span></span>

<span data-ttu-id="97033-106">Se si accede a una classe [*cim*](windows-remote-management-glossary.md) 2,1, ad esempio file di file [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-datafile), il prefisso dell'URI differisce dal prefisso di una classe CIM 2,9, ad esempio **CIM \_ AdminDomain**.</span><span class="sxs-lookup"><span data-stu-id="97033-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="97033-107">Le classi CIM 2,1 sono documentate nella sezione [classi CIM](/windows/desktop/WmiSdk/cimclas) di Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="97033-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="97033-108">La maggior parte delle [classi WMI](/windows/desktop/WmiSdk/wmi-classes) si trova nello spazio dei nomi WMI **\\ CIMV2 radice** .</span><span class="sxs-lookup"><span data-stu-id="97033-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="97033-109">Le classi per il provider Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) si trovano nell' **\\ hardware radice**.</span><span class="sxs-lookup"><span data-stu-id="97033-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="97033-110">Nell'elenco seguente sono inclusi i prefissi URI delle risorse per questi schemi:</span><span class="sxs-lookup"><span data-stu-id="97033-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="97033-111">Classi WMI o CIM 2,1 nello spazio dei nomi **\\ CIMV2 radice**</span><span class="sxs-lookup"><span data-stu-id="97033-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="97033-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="97033-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="97033-113">Classi CIM 2,9 o classi IPMI</span><span class="sxs-lookup"><span data-stu-id="97033-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="97033-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="97033-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="97033-115">Modalità alternativa per accedere alle classi del provider IPMI</span><span class="sxs-lookup"><span data-stu-id="97033-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="97033-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="97033-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="97033-117">Per altre informazioni, vedere [URI di risorsa](resource-uris.md) e [stringhe URLPrefix](/windows/desktop/Http/urlprefix-strings).</span><span class="sxs-lookup"><span data-stu-id="97033-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="97033-118">Per ulteriori informazioni sulla generazione di un URI per una classe o un metodo WMI, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="97033-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="97033-119">Alias di prefisso</span><span class="sxs-lookup"><span data-stu-id="97033-119">Prefix Aliases</span></span>

<span data-ttu-id="97033-120">Un alias di prefisso è un tasto di scelta rapida che rappresenta il prefisso dell'URI di risorsa lungo.</span><span class="sxs-lookup"><span data-stu-id="97033-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="97033-121">È anche possibile usare gli alias nella riga di comando di **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="97033-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="97033-122">Per visualizzare un elenco di alias disponibili, digitare gli **alias della Guida WinRM**.</span><span class="sxs-lookup"><span data-stu-id="97033-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="97033-123">Tenere presente che un alias non può essere usato in un riferimento all'endpoint (EPR) quando si specifica un URI di risorsa.</span><span class="sxs-lookup"><span data-stu-id="97033-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="97033-124">Gestione remota Windows non è in grado di espandere l'alias quando è incorporato in XML.</span><span class="sxs-lookup"><span data-stu-id="97033-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="97033-125">Nell'esempio di codice seguente, l'alias WinRM viene usato in un EPR anziché nell'URI completo della risorsa, ovvero `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` .</span><span class="sxs-lookup"><span data-stu-id="97033-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="97033-126">In questo caso, WinRM restituisce un errore che indica che il servizio non è in grado di elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="97033-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="97033-127">Di seguito sono elencati gli alias definiti e gli URI delle risorse per i quali sostituiscono.</span><span class="sxs-lookup"><span data-stu-id="97033-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="97033-128"><span id="wmi"></span><span id="WMI"></span>WMI</span><span class="sxs-lookup"><span data-stu-id="97033-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="97033-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="97033-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="97033-130"><span id="cimv2"></span><span id="CIMV2"></span>CIMV2</span><span class="sxs-lookup"><span data-stu-id="97033-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="97033-131"><span id="winrm"></span><span id="WINRM"></span>WinRM</span><span class="sxs-lookup"><span data-stu-id="97033-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="97033-132"><span id="wsman"></span><span id="WSMAN"></span>WSMan</span><span class="sxs-lookup"><span data-stu-id="97033-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="97033-133"><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="97033-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="97033-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97033-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97033-135">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="97033-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="97033-136">Gestione remota Windows e WMI</span><span class="sxs-lookup"><span data-stu-id="97033-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="97033-137">URI risorse</span><span class="sxs-lookup"><span data-stu-id="97033-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
