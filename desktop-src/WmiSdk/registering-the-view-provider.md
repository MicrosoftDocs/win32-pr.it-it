---
description: WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione di WMI. Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrazione del provider di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318537"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="63730-104">Registrazione del provider di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="63730-104">Registering the View Provider</span></span>

<span data-ttu-id="63730-105">WMI registra automaticamente la DLL del provider di visualizzazione durante il processo di installazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="63730-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="63730-106">Tuttavia, è comunque necessario registrare il provider di visualizzazione con WMI per ogni spazio dei nomi che conterrà le classi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="63730-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="63730-107">Nella procedura riportata di seguito viene descritto come registrare il provider di viste.</span><span class="sxs-lookup"><span data-stu-id="63730-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="63730-108">**Per registrare il provider di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="63730-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="63730-109">Creare un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) per descrivere l'implementazione del provider di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="63730-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="63730-110">L'istanza di [**\_ \_ Win32Provider**](--win32provider.md) descrive il nome del provider e il relativo identificatore di classe (CLSID), nonché le impostazioni di sicurezza predefinite.</span><span class="sxs-lookup"><span data-stu-id="63730-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="63730-111">Nell'esempio di codice seguente viene descritta un'implementazione di [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="63730-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="63730-112">Creare un'istanza della classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="63730-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="63730-113">Nell'esempio di codice seguente viene illustrato come creare un'istanza della classe **\_ \_ InstanceProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="63730-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="63730-114">Creare un'istanza della classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) se si desidera che i metodi di supporto della classe Union View.</span><span class="sxs-lookup"><span data-stu-id="63730-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="63730-115">Nell'esempio di codice seguente viene illustrato come creare un'istanza della classe **\_ \_ MethodProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="63730-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="63730-116">Compilare il codice MOF usando il compilatore MOF ([mofcomp](mofcomp.md)) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="63730-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="63730-117">Se si salva l'esempio di codice MOF elencato in precedenza in un file denominato Viewtest. mof, utilizzare il comando mofcomp per caricare il codice MOF nello spazio dei nomi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="63730-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="63730-118">*NamespacePath* è lo spazio dei nomi in cui si desidera creare l'istanza della classe di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="63730-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="63730-119">Al prompt dei comandi digitare il comando seguente per caricare il codice MOF nello spazio dei nomi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="63730-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="63730-120">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="63730-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="63730-121">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="63730-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



