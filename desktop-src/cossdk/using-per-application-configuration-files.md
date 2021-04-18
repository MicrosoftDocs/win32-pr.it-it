---
description: Uso di file di configurazione Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Uso di file di configurazione Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4d59d05f6a7b9b894a2577eb55cceffa49d267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304723"
---
# <a name="using-per-application-configuration-files"></a><span data-ttu-id="a300c-103">Uso di file di configurazione Per-Application</span><span class="sxs-lookup"><span data-stu-id="a300c-103">Using Per-Application Configuration Files</span></span>

<span data-ttu-id="a300c-104">Per l'utilizzo di file di configurazione per applicazione COM+ sono necessari i passaggi di base seguenti:</span><span class="sxs-lookup"><span data-stu-id="a300c-104">Using COM+ per-application configuration files requires the following basic steps:</span></span>

-   <span data-ttu-id="a300c-105">Configurare una directory radice dell'applicazione per un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a300c-105">Configure an application root directory for a COM+ application.</span></span>
-   <span data-ttu-id="a300c-106">Creare file Application. manifest e application.config nella directory radice dell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a300c-106">Create application.manifest and application.config files in the COM+ application root directory.</span></span>

> [!Note]  
> <span data-ttu-id="a300c-107">I file di configurazione per applicazione sono disponibili solo a partire da Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a300c-107">Per-application configuration files are only available starting with Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span>

 

<span data-ttu-id="a300c-108">**Per usare un file di configurazione per applicazione**</span><span class="sxs-lookup"><span data-stu-id="a300c-108">**To use a per-application configuration file**</span></span>

1.  <span data-ttu-id="a300c-109">Creare una libreria di classi .NET con un riferimento all'assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="a300c-109">Create a .NET class library, with a reference to the System.EnterpriseServices assembly.</span></span>

2.  <span data-ttu-id="a300c-110">La libreria di classi deve contenere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="a300c-110">The class library should contain the following code:</span></span>

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    <span data-ttu-id="a300c-111">Si noti che "ConfigData1" è un nome di impostazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="a300c-111">Note that "ConfigData1" is a sample setting name.</span></span> <span data-ttu-id="a300c-112">È possibile sostituirlo con il nome dell'impostazione scelta.</span><span class="sxs-lookup"><span data-stu-id="a300c-112">You can replace this with the setting name of your choice.</span></span>

3.  <span data-ttu-id="a300c-113">Creare un'applicazione COM+ vuota.</span><span class="sxs-lookup"><span data-stu-id="a300c-113">Create an empty COM+ application.</span></span> <span data-ttu-id="a300c-114">Per istruzioni su come eseguire questa operazione, vedere [creazione di una nuova applicazione com+](creating-a-new-com--application.md).</span><span class="sxs-lookup"><span data-stu-id="a300c-114">For instructions on how to do this, see [Creating a New COM+ Application](creating-a-new-com--application.md).</span></span>
4.  <span data-ttu-id="a300c-115">Installare la libreria di classi creata nell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a300c-115">Install the class library you created into the COM+ application.</span></span> <span data-ttu-id="a300c-116">Per istruzioni su come eseguire questa operazione, vedere [installazione di nuovi componenti](installing-new-components.md).</span><span class="sxs-lookup"><span data-stu-id="a300c-116">For instructions on how to do this, see [Installing New Components](installing-new-components.md).</span></span>
5.  <span data-ttu-id="a300c-117">Nello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione COM+ creata e selezionare **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="a300c-117">In the Component Services administrative tool, right-click the COM+ application you created and select **Properties**.</span></span>
6.  <span data-ttu-id="a300c-118">Nella finestra di dialogo **Proprietà** selezionare la scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="a300c-118">In the **Properties** dialog box, select the **Activation** tab.</span></span>
7.  <span data-ttu-id="a300c-119">Verificare che il **tipo di attivazione** sia impostato su **applicazione server**.</span><span class="sxs-lookup"><span data-stu-id="a300c-119">Make sure the **Activation type** is set to **Server application**.</span></span>
8.  <span data-ttu-id="a300c-120">Nella casella di testo **directory radice dell'applicazione** immettere il percorso o selezionare la directory in cui si desidera archiviare i file di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a300c-120">In the **Application Root Directory** text box, enter the path or browse to the directory where you want to store your application configuration files for this application.</span></span>
9.  <span data-ttu-id="a300c-121">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="a300c-121">Click **OK**.</span></span>

    <span data-ttu-id="a300c-122">Si noti che è inoltre possibile specificare la directory radice dell'applicazione COM+ tramite la proprietà ApplicationDirectory della classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a300c-122">Note that you can also specify the COM+ application root directory through the ApplicationDirectory property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span> <span data-ttu-id="a300c-123">Per ulteriori informazioni, vedere [**applicazioni**](applications.md).</span><span class="sxs-lookup"><span data-stu-id="a300c-123">For more information, see [**Applications**](applications.md).</span></span>

10. <span data-ttu-id="a300c-124">Nella directory in cui si è scelto di archiviare i file di configurazione dell'applicazione, creare un file denominato *Application*. manifest.</span><span class="sxs-lookup"><span data-stu-id="a300c-124">In the directory you chose to store your application configuration files, create a file named *application*.manifest.</span></span> <span data-ttu-id="a300c-125">Con un editor di testo, aggiungere il testo seguente al file:</span><span class="sxs-lookup"><span data-stu-id="a300c-125">With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. <span data-ttu-id="a300c-126">Nella stessa directory creare un file denominato *Application*. config. Con un editor di testo, aggiungere il testo seguente al file:</span><span class="sxs-lookup"><span data-stu-id="a300c-126">In the same directory, create a file named *application*.config. With a text editor, add the following text to this file:</span></span>

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    <span data-ttu-id="a300c-127">Si noti che questo file di configurazione è solo un esempio.</span><span class="sxs-lookup"><span data-stu-id="a300c-127">Note that this configuration file is just an example.</span></span> <span data-ttu-id="a300c-128">È possibile creare più chiavi con nomi e valori diversi.</span><span class="sxs-lookup"><span data-stu-id="a300c-128">You can create multiple keys with different names and values.</span></span> <span data-ttu-id="a300c-129">Si noti, tuttavia, che "ConfigData1" corrisponde al nome dell'impostazione usato nella libreria di classi creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a300c-129">Note, however, that "ConfigData1" matches the setting name used in the class library created earlier.</span></span>

12. <span data-ttu-id="a300c-130">Creare un'applicazione console .NET, con un riferimento alla libreria di classi .NET creata in precedenza e un riferimento all'assembly System. EnterpriseServices.</span><span class="sxs-lookup"><span data-stu-id="a300c-130">Create a .NET console application, with a reference to the .NET class library you created earlier, and a reference to the System.EnterpriseServices assembly.</span></span>
13. <span data-ttu-id="a300c-131">L'applicazione console deve contenere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="a300c-131">The console application should contain the following code:</span></span>
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

<span data-ttu-id="a300c-132">Eseguire l'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="a300c-132">Run the console application.</span></span> <span data-ttu-id="a300c-133">L'output dovrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="a300c-133">The output should be:</span></span>

``` syntax
Configuration Data Number 1
```

 

 



