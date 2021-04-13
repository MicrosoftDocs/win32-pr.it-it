---
title: Individuazione del profilo DMTF tramite l'attraversamento dell'associazione
description: Un componente chiave dell'infrastruttura di Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399830"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="7ef2a-103">Individuazione del profilo DMTF tramite l'attraversamento dell'associazione</span><span class="sxs-lookup"><span data-stu-id="7ef2a-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="7ef2a-104">Un componente chiave dell'infrastruttura di Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="7ef2a-105">Il modello è conforme a uno standard gestito dal Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) ed è noto come Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="7ef2a-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="7ef2a-106">Alcune classi del modello, ad esempio [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) o [ \_ processo Win32](../cimwin32prov/win32-process.md), corrispondono direttamente a entità gestibili.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="7ef2a-107">Altre classi del modello, ad esempio [Win32 \_ SystemServices](../cimwin32prov/win32-systemservices.md), rappresentano le relazioni tra entità gestibili.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="7ef2a-108">Queste classi di modellazione delle relazioni sono note come classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="7ef2a-109">Utilizzando il linguaggio di query specifico di WMI, WQL, è possibile recuperare istanze di classi che rappresentano entità gestibili o istanze di classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="7ef2a-110">Ma WQL è specifico dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-110">But WQL is implementation specific.</span></span> <span data-ttu-id="7ef2a-111">Funziona solo con l'implementazione di Windows dello standard DMTF (WMI).</span><span class="sxs-lookup"><span data-stu-id="7ef2a-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="7ef2a-112">Inoltre, la sintassi WQL per il recupero delle classi di associazione è piuttosto complessa.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="7ef2a-113">L'infrastruttura di Gestione remota Windows (WinRM) fornisce un modo eccellente per sfruttare le funzionalità di WMI.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="7ef2a-114">Nelle prime versioni di WinRM era necessario utilizzare WQL per recuperare le istanze delle classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="7ef2a-115">WinRM 2,0 include una nuova funzionalità nota come individuazione del profilo DMTF tramite l'attraversamento delle associazioni.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="7ef2a-116">L'attraversamento delle associazioni consente a un utente di WinRM di recuperare le istanze delle classi di associazione usando un meccanismo di filtro standard, il dialetto AssociationFilter, definito nella specifica di associazione CIM di DMTF.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="7ef2a-117">Per ulteriori informazioni sull'attraversamento delle associazioni, vedere la specifica di WS-Management CIM binding ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="7ef2a-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="7ef2a-118">L'utilità WinRM fornisce un meccanismo semplice per attraversare l'associazione appropriata e recuperare un profilo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="7ef2a-119">Dettagli di implementazione della configurazione</span><span class="sxs-lookup"><span data-stu-id="7ef2a-119">Configuration Implementation Details</span></span>

<span data-ttu-id="7ef2a-120">L'utilità WinRM supporta ora un dialetto per la richiesta di associazione.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="7ef2a-121">È possibile specificare l'URI o l'alias utilizzando l'utilità WinRM.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="7ef2a-122">Alias</span><span class="sxs-lookup"><span data-stu-id="7ef2a-122">Alias</span></span>       | <span data-ttu-id="7ef2a-123">URI</span><span class="sxs-lookup"><span data-stu-id="7ef2a-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="7ef2a-124">associazione</span><span class="sxs-lookup"><span data-stu-id="7ef2a-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="7ef2a-125">Recupero di istanze di una classe di associazione tramite il sottolinguaggio AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="7ef2a-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="7ef2a-126">L'utilità WinRM può recuperare le istanze della classe di associazione WMI di una particolare istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="7ef2a-127">Il comando seguente illustra come usare l'utilità WinRM per recuperare le istanze delle classi di associazione al [ \_ servizio Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef2a-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="7ef2a-128">Per restituire le classi di associazione, è necessario utilizzare l'opzione "-Associations".</span><span class="sxs-lookup"><span data-stu-id="7ef2a-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="7ef2a-129">**WinRM enumerate wmicimv2/ \* -dialetto: Association-Associations-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; Role = dipendente}**</span><span class="sxs-lookup"><span data-stu-id="7ef2a-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="7ef2a-130">Il seguente frammento di codice basato su testo è l'output del comando precedente:</span><span class="sxs-lookup"><span data-stu-id="7ef2a-130">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="7ef2a-131">Recupero di istanze di una classe associata tramite il sottolinguaggio AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="7ef2a-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="7ef2a-132">L'utilità WinRM può recuperare le istanze della classe WMI associate a una particolare istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="7ef2a-133">Il comando seguente illustra come usare l'utilità WinRM per recuperare le istanze delle classi associate al [ \_ servizio Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="7ef2a-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="7ef2a-134">**WinRM enumerate wmicimv2/ \* -dialetto: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; RESULTROLE = Antecedent; Role = dipendente}**</span><span class="sxs-lookup"><span data-stu-id="7ef2a-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="7ef2a-135">Il seguente frammento di codice basato su testo è l'output del comando precedente:</span><span class="sxs-lookup"><span data-stu-id="7ef2a-135">The following text-based snippet is the output of the above command:</span></span>

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 