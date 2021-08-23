---
title: Individuazione del profilo DMTF tramite attraversamento di associazione
description: Un componente chiave dell'Windows Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f49d1433d8263dff2c1d50007f9aa0daf1573c09ebc8d7a513eda658c51997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643151"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Individuazione del profilo DMTF tramite attraversamento di associazione

Un componente chiave dell'Windows Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema. Il modello è conforme a uno standard gestito da Desktop Management Task Force[(DMTF)](https://www.dmtf.org/standards/wsman)ed è noto come Common Information Model (CIM). Alcune classi nel modello, ad esempio [CIM \_ DataFile](../cimwin32prov/cim-datafile.md) o [Processo Win32, \_ ](../cimwin32prov/win32-process.md)corrispondono direttamente alle entità gestibili. Altre classi del modello, ad esempio [ \_ SystemServices Win32,](../cimwin32prov/win32-systemservices.md)rappresentano relazioni tra entità gestibili. Queste classi di modellazione delle relazioni sono note come classi di associazione.

Tramite il linguaggio di query specifico di WMI, WQL, è possibile recuperare istanze di classi che rappresentano entità gestibili o istanze di classi di associazione. Tuttavia, WQL è specifico dell'implementazione. Funziona solo con l'implementazione Windows dello standard DMTF (WMI). Inoltre, la sintassi WQL per il recupero delle classi di associazione è piuttosto complessa.

L Windows in infrastruttura di gestione remota (WinRM) offre un ottimo modo per sfruttare le funzionalità di WMI. Le prime versioni di WinRM dovevano usare WQL per recuperare le istanze delle classi association. WinRM 2.0 include una nuova funzionalità nota come individuazione del profilo DMTF tramite attraversamento di associazione. L'attraversamento dell'associazione consente a un utente di WinRM di recuperare le istanze delle classi association usando un meccanismo di filtro standard, il dialetto AssociationFilter, definito nella specifica di associazione CIM DMTF. Per altre informazioni sull'attraversamento dell'associazione, vedere la WS-Management specifica dell'associazione CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

L'utilità winrm fornisce un meccanismo semplice per attraversare l'associazione appropriata e recuperare un profilo di dispositivo.

## <a name="configuration-implementation-details"></a>Dettagli dell'implementazione della configurazione

L'utilità winrm supporta ora un dialetto per la richiesta di associazione. È possibile specificare l'URI o l'alias usando l'utilità winrm.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| associazione | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recupero di istanze di una classe di associazione tramite il dialetto AssociationFilter

L'utilità winrm può recuperare le istanze della classe di associazione WMI di una determinata istanza di origine. Il comando seguente illustra come usare l'utilità winrm per recuperare istanze delle classi di associazione del servizio [Win32. \_ ](../cimwin32prov/win32-service.md) L'opzione "-associations" deve essere usata per restituire classi di associazione.

**winrm enumerate wmicimv2/ \* -dialect:association -associations -filter:{object=win32 \_ service?name=winrm;resultclassname=win32 \_ dependentservice;role=dependent}**

Il frammento di codice basato su testo seguente è l'output del comando precedente:

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Recupero di istanze di una classe associata tramite il dialetto AssociationFilter

L'utilità winrm può recuperare le istanze della classe WMI associate a una determinata istanza di origine. Il comando seguente illustra come usare l'utilità winrm per recuperare le istanze delle classi associate al servizio [Win32. \_ ](../cimwin32prov/win32-service.md)

**winrm enumerate wmicimv2/ \* -dialect:association -filter:{object=win32 \_ service?name=winrm;associationclassname=win32 \_ dependentservice;resultclassname=win32 \_ service;resultrole=antecedent;role=dependent}**

Il frammento di codice basato su testo seguente è l'output del comando precedente:

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

 

 