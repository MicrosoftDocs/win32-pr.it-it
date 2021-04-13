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
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Individuazione del profilo DMTF tramite l'attraversamento dell'associazione

Un componente chiave dell'infrastruttura di Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema. Il modello è conforme a uno standard gestito dal Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) ed è noto come Common Information Model (CIM). Alcune classi del modello, ad esempio [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) o [ \_ processo Win32](../cimwin32prov/win32-process.md), corrispondono direttamente a entità gestibili. Altre classi del modello, ad esempio [Win32 \_ SystemServices](../cimwin32prov/win32-systemservices.md), rappresentano le relazioni tra entità gestibili. Queste classi di modellazione delle relazioni sono note come classi di associazione.

Utilizzando il linguaggio di query specifico di WMI, WQL, è possibile recuperare istanze di classi che rappresentano entità gestibili o istanze di classi di associazione. Ma WQL è specifico dell'implementazione. Funziona solo con l'implementazione di Windows dello standard DMTF (WMI). Inoltre, la sintassi WQL per il recupero delle classi di associazione è piuttosto complessa.

L'infrastruttura di Gestione remota Windows (WinRM) fornisce un modo eccellente per sfruttare le funzionalità di WMI. Nelle prime versioni di WinRM era necessario utilizzare WQL per recuperare le istanze delle classi di associazione. WinRM 2,0 include una nuova funzionalità nota come individuazione del profilo DMTF tramite l'attraversamento delle associazioni. L'attraversamento delle associazioni consente a un utente di WinRM di recuperare le istanze delle classi di associazione usando un meccanismo di filtro standard, il dialetto AssociationFilter, definito nella specifica di associazione CIM di DMTF. Per ulteriori informazioni sull'attraversamento delle associazioni, vedere la specifica di WS-Management CIM binding ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

L'utilità WinRM fornisce un meccanismo semplice per attraversare l'associazione appropriata e recuperare un profilo di dispositivo.

## <a name="configuration-implementation-details"></a>Dettagli di implementazione della configurazione

L'utilità WinRM supporta ora un dialetto per la richiesta di associazione. È possibile specificare l'URI o l'alias utilizzando l'utilità WinRM.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| associazione | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recupero di istanze di una classe di associazione tramite il sottolinguaggio AssociationFilter

L'utilità WinRM può recuperare le istanze della classe di associazione WMI di una particolare istanza di origine. Il comando seguente illustra come usare l'utilità WinRM per recuperare le istanze delle classi di associazione al [ \_ servizio Win32](../cimwin32prov/win32-service.md) . Per restituire le classi di associazione, è necessario utilizzare l'opzione "-Associations".

**WinRM enumerate wmicimv2/ \* -dialetto: Association-Associations-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; Role = dipendente}**

Il seguente frammento di codice basato su testo è l'output del comando precedente:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Recupero di istanze di una classe associata tramite il sottolinguaggio AssociationFilter

L'utilità WinRM può recuperare le istanze della classe WMI associate a una particolare istanza di origine. Il comando seguente illustra come usare l'utilità WinRM per recuperare le istanze delle classi associate al [ \_ servizio Win32](../cimwin32prov/win32-service.md) .

**WinRM enumerate wmicimv2/ \* -dialetto: Association-Filter: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; RESULTROLE = Antecedent; Role = dipendente}**

Il seguente frammento di codice basato su testo è l'output del comando precedente:

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

 

 