---
description: Il provider del registro di sistema viene registrato come parte del processo di installazione di WMI in Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registrazione del provider del registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309912"
---
# <a name="registering-the-system-registry-provider"></a>Registrazione del provider del registro di sistema

Il provider del registro di sistema viene registrato come parte del processo di installazione di WMI in Windows. Se si utilizza un'altra piattaforma e si desidera utilizzare il provider del registro di sistema, è necessario prima registrare il provider seguendo la procedura descritta di seguito.

Nella procedura riportata di seguito viene descritto come registrare il provider del registro di sistema.

**Per registrare il provider del registro di sistema**

1.  Registrare il provider come server COM.

    Se necessario, potrebbe essere necessario creare voci del registro di sistema. Questo processo si applica a tutti i server COM e non è correlato a WMI. Per ulteriori informazioni, vedere la documentazione [com](https://msdn.microsoft.com/library/aa139695.aspx) in Microsoft Windows Software Development Kit (SDK).

2.  Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider del registro di sistema.

    L'istanza di [**\_ \_ Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (**CLSID**).

    Nell'esempio seguente viene illustrato come registrare [**\_ \_ Win32Provider**](--win32provider.md) come proprietà di istanza, evento o provider di metodi.

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

3.  Creare una o più istanze delle classi derivate dalla classe [**\_ \_ ProviderRegistration**](--providerregistration.md) per descrivere l'implementazione logica del provider del registro di sistema.

    A seconda dello scopo per cui si registra il provider del registro di sistema, è possibile creare una o più delle classi seguenti.

    [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)

    [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)

    [**\_\_EventProviderRegistration**](--eventproviderregistration.md)

    [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)

    Nell'esempio di codice MOF riportato di seguito viene illustrato come registrare il provider del registro di sistema come un'istanza, una proprietà, un evento o un provider di metodi.

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

4.  Compilare il file MOF utilizzando il compilatore MOF o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

Il file regevent. mof fornito nella sezione WMI del Windows SDK contiene le istanze [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necessarie per registrare il provider del registro di sistema come provider di eventi. Per ulteriori informazioni sulla registrazione di un provider, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md) e alla [ricezione di un evento WMI](receiving-a-wmi-event.md).

 

 



