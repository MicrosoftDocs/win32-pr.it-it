---
description: WMI fornisce un'interfaccia uniforme per tutte le applicazioni locali o remote o script che ottengono dati di gestione da un sistema di computer, una rete o un'azienda.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Architettura WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562742"
---
# <a name="wmi-architecture"></a><span data-ttu-id="32e47-103">Architettura WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-103">WMI Architecture</span></span>

<span data-ttu-id="32e47-104">WMI fornisce un'interfaccia uniforme per tutte le applicazioni locali o remote o script che ottengono dati di gestione da un sistema di computer, una rete o un'azienda.</span><span class="sxs-lookup"><span data-stu-id="32e47-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="32e47-105">L'interfaccia uniforme è progettata in modo che le applicazioni e gli script client WMI non debbano chiamare un'ampia gamma di API (Application Programming Interface) del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32e47-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="32e47-106">Molte API non possono essere chiamate da client di automazione come script o applicazioni Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="32e47-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="32e47-107">Altre API non eseguono chiamate a computer remoti.</span><span class="sxs-lookup"><span data-stu-id="32e47-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="32e47-108">Per ottenere dati da WMI, scrivere uno script client o un'applicazione che accede a [classi WMI](wmi-classes.md) o fornire dati a WMI scrivendo un [*provider WMI*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="32e47-109">Per ulteriori informazioni, vedere [utilizzo di WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="32e47-110">Oggetti, consumer e infrastruttura di WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="32e47-111">Nel diagramma seguente viene illustrata la relazione tra l'infrastruttura WMI e i provider WMI e gli oggetti gestiti e viene inoltre illustrata la relazione tra l'infrastruttura WMI e i consumer WMI.</span><span class="sxs-lookup"><span data-stu-id="32e47-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![relazione tra l'infrastruttura WMI, i provider WMI e gli oggetti gestiti](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="32e47-113">Componenti WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-113">WMI Components</span></span>

<span data-ttu-id="32e47-114">Nell'elenco seguente vengono descritti i principali componenti WMI:</span><span class="sxs-lookup"><span data-stu-id="32e47-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="32e47-115">Oggetti gestiti e provider WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="32e47-116">Un provider WMI è un oggetto COM che monitora uno o più [*oggetti gestiti*](gloss-m.md) per WMI.</span><span class="sxs-lookup"><span data-stu-id="32e47-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="32e47-117">Un oggetto gestito è un componente aziendale logico o fisico, ad esempio un'unità disco rigido, una scheda di rete, un sistema di database, un sistema operativo, un processo o un servizio.</span><span class="sxs-lookup"><span data-stu-id="32e47-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="32e47-118">Analogamente a un driver, un provider fornisce WMI con dati da un oggetto gestito e gestisce i messaggi da WMI all'oggetto gestito.</span><span class="sxs-lookup"><span data-stu-id="32e47-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="32e47-119">I provider WMI sono costituiti da un file DLL e da un file [*Managed Object Format (MOF)*](gloss-m.md) che definisce le classi per le quali il provider restituisce i dati ed esegue operazioni.</span><span class="sxs-lookup"><span data-stu-id="32e47-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="32e47-120">I provider, come le applicazioni WMI C++, usano l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="32e47-121">Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="32e47-122">Un esempio di provider è il [provider del registro](/previous-versions/windows/desktop/regprov/system-registry-provider)preinstallato, che accede ai dati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="32e47-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="32e47-123">Il provider del registro di sistema dispone di una [*classe WMI*](gloss-w.md), [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), con molti metodi ma senza proprietà.</span><span class="sxs-lookup"><span data-stu-id="32e47-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="32e47-124">Altri provider preinstallati, ad esempio il [provider Win32](/windows/desktop/CIMWin32Prov/win32-provider), dispongono in genere di classi con molte proprietà ma con pochi metodi, come il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) o [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="32e47-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="32e47-125">Il file DLL del provider del registro di sistema, Stdprov.dll, contiene il codice che restituisce dinamicamente i dati quando richiesto dagli script client o dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="32e47-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="32e47-126">I file MOF e DLL di WMI si trovano in% WINDIR% \\ system32 \\ WBEM, insieme agli [strumenti di Command-Line WMI](wmi-command-line-tools.md), ad esempio [**Winmgmt.exe**](winmgmt.md) e [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="32e47-127">Le classi provider, ad esempio [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), sono definite nei file MOF e quindi compilate nel repository WMI all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="32e47-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="32e47-128">Infrastruttura WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="32e47-129">L'infrastruttura WMI è un componente del sistema operativo Microsoft Windows noto come servizio WMI (Winmgmt).</span><span class="sxs-lookup"><span data-stu-id="32e47-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="32e47-130">L'infrastruttura WMI è costituita da due componenti: il nucleo WMI e il [*repository WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="32e47-131">Il repository WMI è organizzato in base agli [*spazi dei nomi*](gloss-n.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="32e47-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="32e47-132">Il servizio WMI crea alcuni spazi dei nomi, ad esempio radice radice \\ , radice \\ CIMV2 e \\ sottoscrizione radice all'avvio del sistema e preinstalla un set predefinito di definizioni di classe, incluse le [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider), le [classi di sistema WMI](wmi-system-classes.md)e altre.</span><span class="sxs-lookup"><span data-stu-id="32e47-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="32e47-133">Gli spazi dei nomi rimanenti presenti nel sistema vengono creati dai provider per altre parti del sistema operativo o dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="32e47-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="32e47-134">Per ulteriori informazioni e per un elenco di provider WMI disponibili nella maggior parte delle versioni del sistema operativo, vedere [provider WMI](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="32e47-135">Il servizio WMI funge da intermediario tra i provider, le applicazioni di gestione e il repository WMI.</span><span class="sxs-lookup"><span data-stu-id="32e47-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="32e47-136">Solo i dati statici sugli oggetti vengono archiviati nel repository, ad esempio le classi definite dai provider.</span><span class="sxs-lookup"><span data-stu-id="32e47-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="32e47-137">WMI ottiene la maggior parte dei dati dinamicamente dal provider quando viene richiesto da un client.</span><span class="sxs-lookup"><span data-stu-id="32e47-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="32e47-138">È anche possibile impostare le sottoscrizioni per ricevere notifiche degli eventi da un provider.</span><span class="sxs-lookup"><span data-stu-id="32e47-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="32e47-139">Per ulteriori informazioni, vedere [monitoraggio degli eventi](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="32e47-140">Consumer WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-140">WMI consumers</span></span>

    <span data-ttu-id="32e47-141">Un consumer WMI è un'applicazione di gestione o uno script che interagisce con l'infrastruttura WMI.</span><span class="sxs-lookup"><span data-stu-id="32e47-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="32e47-142">Un'applicazione di gestione può eseguire query, enumerare dati, eseguire metodi del provider o sottoscrivere eventi chiamando l' [API com per WMI](com-api-for-wmi.md) o l' [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="32e47-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="32e47-143">Gli unici dati o azioni disponibili per un oggetto gestito, ad esempio un'unità disco o un servizio, sono quelli forniti da un provider.</span><span class="sxs-lookup"><span data-stu-id="32e47-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32e47-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32e47-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32e47-145">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="32e47-146">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="32e47-147">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="32e47-148">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="32e47-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="32e47-149">Invio di dati a WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="32e47-150">Classi WMI</span><span class="sxs-lookup"><span data-stu-id="32e47-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="32e47-151">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="32e47-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="32e47-152">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="32e47-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
