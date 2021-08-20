---
description: Il provider del Registro di sistema viene registrato come parte del processo di installazione WMI Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registrazione del provider del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45ea97228038b173ef89cac85b9efab1385938fcaac3b2bf0d733be9f34dabe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992501"
---
# <a name="registering-the-system-registry-provider"></a>Registrazione del provider del Registro di sistema

Il provider del Registro di sistema viene registrato come parte del processo di installazione WMI Windows. Se si usa un'altra piattaforma e si vuole usare il provider del Registro di sistema, è necessario prima registrare il provider seguendo la procedura descritta di seguito.

Nella procedura seguente viene descritto come registrare il provider del Registro di sistema.

**Per registrare il provider del Registro di sistema**

1.  Registrare il provider come server COM.

    Se necessario, potrebbe essere necessario creare voci del Registro di sistema. Questo processo si applica a tutti i server COM e non è correlato a WMI. Per altre informazioni, vedere la [documentazione COM](https://msdn.microsoft.com/library/aa139695.aspx) in Microsoft Windows Software Development Kit (SDK).

2.  Creare un'istanza della [**\_ \_ classe Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider del Registro di sistema.

    [**\_ \_ L'istanza Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (**CLSID**).

    L'esempio seguente descrive come registrare [**\_ \_ Win32Provider**](--win32provider.md) come proprietà di istanza, evento o provider di metodi.

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  Creare una o più istanze di classi derivate dalla [**\_ \_ classe ProviderRegistration**](--providerregistration.md) per descrivere l'implementazione logica del provider del Registro di sistema.

    A seconda dello scopo per cui si sta registrando il provider del Registro di sistema, è possibile creare una o più delle classi seguenti.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    Nell'esempio di codice MOF seguente viene descritto come registrare il provider del Registro di sistema come provider di istanza, proprietà, evento o metodo.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  Compilare il file MOF usando il compilatore MOF o [**l'interfaccia IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

Il file RegEvent.mof fornito nella sezione WMI di Windows SDK contiene le istanze [**\_ \_ Win32Provider**](--win32provider.md) ed [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necessarie per registrare il provider del Registro di sistema come provider di eventi. Per altre informazioni sulla registrazione di un provider, vedere [Registrazione di un provider](registering-a-provider.md) e Ricezione di un evento [WMI.](receiving-a-wmi-event.md)

 

 



