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
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="98699-103">Registrazione del provider del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="98699-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="98699-104">Il provider del registro di sistema viene registrato come parte del processo di installazione di WMI in Windows.</span><span class="sxs-lookup"><span data-stu-id="98699-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="98699-105">Se si utilizza un'altra piattaforma e si desidera utilizzare il provider del registro di sistema, è necessario prima registrare il provider seguendo la procedura descritta di seguito.</span><span class="sxs-lookup"><span data-stu-id="98699-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="98699-106">Nella procedura riportata di seguito viene descritto come registrare il provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="98699-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="98699-107">**Per registrare il provider del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="98699-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="98699-108">Registrare il provider come server COM.</span><span class="sxs-lookup"><span data-stu-id="98699-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="98699-109">Se necessario, potrebbe essere necessario creare voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="98699-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="98699-110">Questo processo si applica a tutti i server COM e non è correlato a WMI.</span><span class="sxs-lookup"><span data-stu-id="98699-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="98699-111">Per ulteriori informazioni, vedere la documentazione [com](https://msdn.microsoft.com/library/aa139695.aspx) in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="98699-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="98699-112">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="98699-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="98699-113">L'istanza di [**\_ \_ Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="98699-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="98699-114">Nell'esempio seguente viene illustrato come registrare [**\_ \_ Win32Provider**](--win32provider.md) come proprietà di istanza, evento o provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="98699-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

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

3.  <span data-ttu-id="98699-115">Creare una o più istanze delle classi derivate dalla classe [**\_ \_ ProviderRegistration**](--providerregistration.md) per descrivere l'implementazione logica del provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="98699-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="98699-116">A seconda dello scopo per cui si registra il provider del registro di sistema, è possibile creare una o più delle classi seguenti.</span><span class="sxs-lookup"><span data-stu-id="98699-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="98699-117">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="98699-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="98699-118">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="98699-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="98699-119">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="98699-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="98699-120">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="98699-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="98699-121">Nell'esempio di codice MOF riportato di seguito viene illustrato come registrare il provider del registro di sistema come un'istanza, una proprietà, un evento o un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="98699-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

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

4.  <span data-ttu-id="98699-122">Compilare il file MOF utilizzando il compilatore MOF o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="98699-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="98699-123">Il file regevent. mof fornito nella sezione WMI del Windows SDK contiene le istanze [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necessarie per registrare il provider del registro di sistema come provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="98699-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="98699-124">Per ulteriori informazioni sulla registrazione di un provider, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md) e alla [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="98699-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



