---
title: Abilitazione degli stili di visualizzazione
description: Questo argomento illustra come configurare l'applicazione per garantire che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102170"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="3a69a-103">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3a69a-103">Enabling Visual Styles</span></span>

<span data-ttu-id="3a69a-104">Questo argomento illustra come configurare l'applicazione per garantire che i controlli comuni siano visualizzati nello stile di visualizzazione preferito dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="3a69a-105">In questo argomento sono incluse le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a69a-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="3a69a-106">Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="3a69a-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="3a69a-107">Uso ComCtl32.dll versione 6 in un'applicazione che usa solo estensioni standard</span><span class="sxs-lookup"><span data-stu-id="3a69a-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="3a69a-108">Uso di ComCtl32 versione 6 in Pannello di controllo o una DLL eseguita da RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="3a69a-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="3a69a-109">Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL che viene portata in un processo</span><span class="sxs-lookup"><span data-stu-id="3a69a-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="3a69a-110">Disattivazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3a69a-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="3a69a-111">Uso degli stili di visualizzazione con contenuto HTML</span><span class="sxs-lookup"><span data-stu-id="3a69a-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="3a69a-112">Quando gli stili di visualizzazione non vengono applicati</span><span class="sxs-lookup"><span data-stu-id="3a69a-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="3a69a-113">Rendere l'applicazione compatibile con le versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="3a69a-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="3a69a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a69a-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="3a69a-115">Uso di manifesti o direttive per garantire che gli stili di visualizzazione possano essere applicati alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="3a69a-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="3a69a-116">Per consentire all'applicazione di usare gli stili di visualizzazione, è necessario usare ComCtl32.dll versione 6 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3a69a-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="3a69a-117">Poiché la versione 6 non è ridistribuibile, è disponibile solo quando l'applicazione è in esecuzione in una versione di Windows che la contiene.</span><span class="sxs-lookup"><span data-stu-id="3a69a-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="3a69a-118">Windows viene fornito sia con la versione 5 che con la versione 6.</span><span class="sxs-lookup"><span data-stu-id="3a69a-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="3a69a-119">ComCtl32.dll versione 6 contiene sia i controlli utente che i controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="3a69a-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="3a69a-120">Per impostazione predefinita, le applicazioni usano i controlli utente definiti in User32.dll e i controlli comuni definiti in ComCtl32.dll versione 5.</span><span class="sxs-lookup"><span data-stu-id="3a69a-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="3a69a-121">Per un elenco delle versioni dll e delle relative piattaforme di distribuzione, vedere [Versioni di controllo comuni](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3a69a-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="3a69a-122">Se si vuole che l'applicazione usi gli stili di visualizzazione, è necessario aggiungere un manifesto dell'applicazione o una direttiva del compilatore che indichi che è necessario usare ComCtl32.dll versione 6, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="3a69a-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="3a69a-123">Un manifesto dell'applicazione consente a un'applicazione di specificare le versioni di un assembly necessarie.</span><span class="sxs-lookup"><span data-stu-id="3a69a-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="3a69a-124">In Microsoft Win32 un assembly è un set di DLL e un elenco di oggetti versionable contenuti all'interno di tali DLL.</span><span class="sxs-lookup"><span data-stu-id="3a69a-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="3a69a-125">I manifesti vengono scritti in XML.</span><span class="sxs-lookup"><span data-stu-id="3a69a-125">Manifests are written in XML.</span></span> <span data-ttu-id="3a69a-126">Il nome del file manifesto dell'applicazione è il nome del file eseguibile seguito dall'estensione .manifest. ad esempio MyApp.exe.manifest.</span><span class="sxs-lookup"><span data-stu-id="3a69a-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="3a69a-127">Il manifesto di esempio seguente mostra che la prima sezione descrive il manifesto stesso.</span><span class="sxs-lookup"><span data-stu-id="3a69a-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="3a69a-128">Nella tabella seguente vengono illustrati gli attributi impostati **dall'elemento assemblyIdentity** nella sezione relativa alla descrizione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="3a69a-129">Attributo</span><span class="sxs-lookup"><span data-stu-id="3a69a-129">Attribute</span></span>             | <span data-ttu-id="3a69a-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a69a-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a69a-131">version</span><span class="sxs-lookup"><span data-stu-id="3a69a-131">version</span></span>               | <span data-ttu-id="3a69a-132">Versione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-132">Version of the manifest.</span></span> <span data-ttu-id="3a69a-133">La versione deve essere nel formato major.minor.revision.build, ovvero n.n.n.n.n, dove n <=65535).</span><span class="sxs-lookup"><span data-stu-id="3a69a-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="3a69a-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="3a69a-134">processorArchitecture</span></span> | <span data-ttu-id="3a69a-135">Processore per cui viene sviluppata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="3a69a-136">name</span><span class="sxs-lookup"><span data-stu-id="3a69a-136">name</span></span>                  | <span data-ttu-id="3a69a-137">Include il nome della società, il nome del prodotto e il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="3a69a-138">tipo</span><span class="sxs-lookup"><span data-stu-id="3a69a-138">type</span></span>                  | <span data-ttu-id="3a69a-139">Tipo dell'applicazione, ad esempio Win32.</span><span class="sxs-lookup"><span data-stu-id="3a69a-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="3a69a-140">Il manifesto di esempio fornisce anche una descrizione dell'applicazione e specifica le dipendenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="3a69a-141">Nella tabella seguente vengono illustrati gli attributi impostati **dall'elemento assemblyIdentity** nella sezione dependency.</span><span class="sxs-lookup"><span data-stu-id="3a69a-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="3a69a-142">Attributo</span><span class="sxs-lookup"><span data-stu-id="3a69a-142">Attribute</span></span>             | <span data-ttu-id="3a69a-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a69a-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="3a69a-144">type</span><span class="sxs-lookup"><span data-stu-id="3a69a-144">type</span></span>                  | <span data-ttu-id="3a69a-145">Tipo del componente di dipendenza, ad esempio Win32.</span><span class="sxs-lookup"><span data-stu-id="3a69a-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="3a69a-146">name</span><span class="sxs-lookup"><span data-stu-id="3a69a-146">name</span></span>                  | <span data-ttu-id="3a69a-147">Nome del componente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-147">Name of the component.</span></span>                           |
| <span data-ttu-id="3a69a-148">version</span><span class="sxs-lookup"><span data-stu-id="3a69a-148">version</span></span>               | <span data-ttu-id="3a69a-149">Versione del componente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-149">Version of the component.</span></span>                        |
| <span data-ttu-id="3a69a-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="3a69a-150">processorArchitecture</span></span> | <span data-ttu-id="3a69a-151">Processore per cui è progettato il componente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="3a69a-152">Publickeytoken</span><span class="sxs-lookup"><span data-stu-id="3a69a-152">publicKeyToken</span></span>        | <span data-ttu-id="3a69a-153">Token di chiave usato con questo componente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="3a69a-154">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="3a69a-154">language</span></span>              | <span data-ttu-id="3a69a-155">Lingua del componente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="3a69a-156">Di seguito è riportato un esempio di file manifesto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a69a-157">Impostare la voce **processorArchitecture** su **"X86"** se l'applicazione è destinata alla piattaforma Windows a 32 bit o **su "amd64"** se l'applicazione è destinata alla piattaforma Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="3a69a-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="3a69a-158">È anche possibile specificare **" \* "**, che garantisce che tutte le piattaforme siano destinate, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a69a-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="3a69a-159">Se si usa Microsoft Visual C++ 2005 o versione successiva, è possibile aggiungere la direttiva del compilatore seguente al codice sorgente anziché creare manualmente un manifesto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="3a69a-160">Per motivi di leggibilità, la direttiva è suddivisa in diverse righe.</span><span class="sxs-lookup"><span data-stu-id="3a69a-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="3a69a-161">Negli argomenti seguenti vengono descritti i passaggi per l'applicazione di stili di visualizzazione a diversi tipi di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3a69a-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="3a69a-162">Si noti che il formato del manifesto è lo stesso in ogni caso.</span><span class="sxs-lookup"><span data-stu-id="3a69a-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="3a69a-163">Uso ComCtl32.dll versione 6 in un'applicazione che usa solo estensioni standard</span><span class="sxs-lookup"><span data-stu-id="3a69a-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="3a69a-164">Di seguito sono riportati esempi di applicazioni che non usano estensioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="3a69a-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="3a69a-165">Calcolatrice</span><span class="sxs-lookup"><span data-stu-id="3a69a-165">Calculator</span></span>
-   <span data-ttu-id="3a69a-166">FreeCell (in Windows Vista e Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a69a-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="3a69a-167">Minesweeper (in Windows Vista e Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a69a-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="3a69a-168">Blocco note</span><span class="sxs-lookup"><span data-stu-id="3a69a-168">Notepad</span></span>
-   <span data-ttu-id="3a69a-169">Solitaire (in Windows Vista e Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3a69a-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="3a69a-170">**Per creare un manifesto e abilitare l'applicazione all'uso degli stili di visualizzazione.**</span><span class="sxs-lookup"><span data-stu-id="3a69a-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="3a69a-171">Collegarsi a ComCtl32.lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="3a69a-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="3a69a-172">Aggiungere un file denominato YourApp.exe.manifest all'albero di origine con il formato manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="3a69a-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="3a69a-173">Aggiungere il manifesto al file di risorse dell'applicazione come segue:</span><span class="sxs-lookup"><span data-stu-id="3a69a-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="3a69a-174">Quando si aggiunge la voce precedente alla risorsa, è necessario formattarla in un'unica riga.</span><span class="sxs-lookup"><span data-stu-id="3a69a-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="3a69a-175">In alternativa, è possibile inserire il file manifesto XML nella stessa directory del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="3a69a-176">Il sistema operativo carica prima il manifesto dal file system, quindi controlla la sezione delle risorse del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3a69a-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="3a69a-177">La file system precedente ha la precedenza.</span><span class="sxs-lookup"><span data-stu-id="3a69a-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="3a69a-178">Quando si compila l'applicazione, il manifesto verrà aggiunto come risorsa binaria.</span><span class="sxs-lookup"><span data-stu-id="3a69a-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="3a69a-179">Uso di ComCtl32 versione 6 in Pannello di controllo o una DLL eseguita da RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="3a69a-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="3a69a-180">**Per creare un manifesto e abilitare l'applicazione all'uso degli stili di visualizzazione.**</span><span class="sxs-lookup"><span data-stu-id="3a69a-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="3a69a-181">Collegarsi a ComCtl32.lib e chiamare [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="3a69a-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="3a69a-182">Aggiungere un file denominato YourApp.cpl.manifest all'albero di origine con il formato manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="3a69a-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="3a69a-183">Aggiungere il manifesto al file di risorse dell'applicazione come ID risorsa 123.</span><span class="sxs-lookup"><span data-stu-id="3a69a-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="3a69a-184">Quando si crea un'Pannello di controllo, posizionarla nella categoria appropriata.</span><span class="sxs-lookup"><span data-stu-id="3a69a-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="3a69a-185">Pannello di controllo ora supporta la categorizzazione Pannello di controllo applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3a69a-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="3a69a-186">Ciò significa che Pannello di controllo applicazioni possono essere assegnate identificatori e separate in aree attività come Installazione applicazioni, Aspetto e temi o Data, Ora, Lingua e Opzioni internazionali.</span><span class="sxs-lookup"><span data-stu-id="3a69a-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="3a69a-187">Aggiunta del supporto dello stile di visualizzazione a un'estensione, un plug-in, uno snap-in MMC o una DLL che viene portata in un processo</span><span class="sxs-lookup"><span data-stu-id="3a69a-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="3a69a-188">È possibile aggiungere il supporto per gli stili di visualizzazione a un'estensione, a un plug-in, a uno snap-in MMC o a una DLL che viene portata in un processo.</span><span class="sxs-lookup"><span data-stu-id="3a69a-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="3a69a-189">Ad esempio, usare la procedura seguente per aggiungere il supporto degli stili di visualizzazione per uno snap-in Microsoft Management Console (MMC).</span><span class="sxs-lookup"><span data-stu-id="3a69a-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="3a69a-190">Compilare lo snap-in con il flag -DISOLATION AWARE ENABLED o inserire l'istruzione seguente prima dell'istruzione \_ \_ di inclusione \# "windows.h".</span><span class="sxs-lookup"><span data-stu-id="3a69a-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="3a69a-191">Per altre informazioni su ISOLATION \_ AWARE \_ ENABLED, vedere [Isolamento dei componenti](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="3a69a-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="3a69a-192">Includere il file di intestazione del controllo comune nell'origine snap-in.</span><span class="sxs-lookup"><span data-stu-id="3a69a-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="3a69a-193">Aggiungere un file denominato YourApp.manifest all'albero di origine che usa il formato manifesto XML.</span><span class="sxs-lookup"><span data-stu-id="3a69a-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="3a69a-194">Aggiungere il manifesto al file di risorse dello snap-in.</span><span class="sxs-lookup"><span data-stu-id="3a69a-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="3a69a-195">Per informazioni dettagliate sull'aggiunta di un manifesto a un file di risorse, vedere Using [ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process (Uso di ComCtl32 versione 6 in](/previous-versions//ms649781(v=vs.85)) un'applicazione che usa estensioni, plug-in o DLL che vengono aggiunti a un processo) per informazioni dettagliate sull'aggiunta di un manifesto a un file di risorse.</span><span class="sxs-lookup"><span data-stu-id="3a69a-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="3a69a-196">Disattivazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3a69a-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="3a69a-197">È possibile disattivare gli stili di visualizzazione per un controllo o per tutti i controlli in una finestra chiamando la [**funzione SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="3a69a-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="3a69a-198">Nell'esempio precedente *hwnd* è l'handle della finestra in cui disabilitare gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="3a69a-199">Dopo la chiamata, il rendering del controllo viene eseguito senza stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="3a69a-200">Uso degli stili di visualizzazione con contenuto HTML</span><span class="sxs-lookup"><span data-stu-id="3a69a-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="3a69a-201">Alle pagine HTML che modificano le Cascading Style Sheets (CSS), ad esempio sfondo o bordo, non sono stati applicati stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="3a69a-202">Visualizzano l'attributo CSS specificato.</span><span class="sxs-lookup"><span data-stu-id="3a69a-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="3a69a-203">Quando viene specificata come parte del contenuto, la maggior parte delle proprietà CSS si applica agli elementi a cui sono applicati stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="3a69a-204">Per impostazione predefinita, gli stili di visualizzazione vengono applicati ai controlli HTML intrinseci nelle pagine visualizzate in Microsoft Internet Explorer 6 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a69a-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="3a69a-205">Per disattivare gli stili di visualizzazione per una pagina HTML, aggiungere un tag META a</span><span class="sxs-lookup"><span data-stu-id="3a69a-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="3a69a-206">.</span><span class="sxs-lookup"><span data-stu-id="3a69a-206">section.</span></span> <span data-ttu-id="3a69a-207">Questa tecnica si applica anche al contenuto in pacchetto come applicazioni HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="3a69a-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="3a69a-208">Per disattivare gli stili di visualizzazione, il tag META deve essere il seguente:</span><span class="sxs-lookup"><span data-stu-id="3a69a-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="3a69a-209">Se l'impostazione del browser e l'impostazione del tag non sono d'accordo, la pagina non applica gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="3a69a-210">Ad esempio, se il tag META è impostato su "no" e il browser è impostato per abilitare gli stili di visualizzazione, gli stili di visualizzazione non verranno applicati alla pagina.</span><span class="sxs-lookup"><span data-stu-id="3a69a-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="3a69a-211">Tuttavia, se il browser o il tag META è impostato su "sì" e l'altro elemento non è specificato, verranno applicati gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="3a69a-212">Gli stili di visualizzazione possono modificare il layout del contenuto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="3a69a-213">Inoltre, se si impostano determinati attributi su controlli HTML intrinseci, ad esempio la larghezza di un pulsante, è possibile che l'etichetta del pulsante sia illeggibile in determinati stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="3a69a-214">È necessario testare accuratamente il contenuto usando gli stili di visualizzazione per determinare se l'applicazione di stili di visualizzazione ha un effetto negativo sul contenuto e sul layout.</span><span class="sxs-lookup"><span data-stu-id="3a69a-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="3a69a-215">Quando gli stili di visualizzazione non vengono applicati</span><span class="sxs-lookup"><span data-stu-id="3a69a-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="3a69a-216">Per evitare di applicare gli stili di visualizzazione a una finestra di primo livello, assegnare alla finestra un'area non Null (**SetWindowRgn**).</span><span class="sxs-lookup"><span data-stu-id="3a69a-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="3a69a-217">Il sistema presuppone che una finestra con un'area non NULL sia una finestra specializzata che non usa gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a69a-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="3a69a-218">Una finestra figlio associata a una finestra di primo livello non di stili di visualizzazione può comunque applicare gli stili di visualizzazione anche se la finestra padre non lo fa.</span><span class="sxs-lookup"><span data-stu-id="3a69a-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="3a69a-219">Se si vuole disabilitare l'uso degli stili di visualizzazione per tutte le finestre nell'applicazione, chiamare [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e non passare il flag STAP \_ ALLOW \_ NONCLIENT.</span><span class="sxs-lookup"><span data-stu-id="3a69a-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="3a69a-220">Se un'applicazione non chiama **SetThemeAppProperties,** i valori del flag presunti sono STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT.</span><span class="sxs-lookup"><span data-stu-id="3a69a-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="3a69a-221">I valori presunti determinano l'applicazione di uno stile di visualizzazione all'area non client, ai controlli e al contenuto Web.</span><span class="sxs-lookup"><span data-stu-id="3a69a-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="3a69a-222">Rendere l'applicazione compatibile con le versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="3a69a-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="3a69a-223">Gran parte dell'architettura dello stile di visualizzazione è progettata per semplificare la spedizione del prodotto nelle versioni precedenti di Windows che non supportano la modifica dell'aspetto dei controlli.</span><span class="sxs-lookup"><span data-stu-id="3a69a-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="3a69a-224">Quando si spediva un'applicazione per più di un sistema operativo, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3a69a-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="3a69a-225">Nelle versioni di Windows precedenti a Windows 8, gli stili di visualizzazione sono disattivati quando il contrasto elevato è on.</span><span class="sxs-lookup"><span data-stu-id="3a69a-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="3a69a-226">Per supportare il contrasto elevato, un'applicazione legacy che supporta gli stili di visualizzazione deve fornire un percorso di codice separato per disegnare correttamente gli elementi dell'interfaccia utente a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="3a69a-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="3a69a-227">In Windows 8, il contrasto elevato fa parte degli stili di visualizzazione. Tuttavia, un'applicazione Windows 8 (che include il GUID Windows 8 nella sezione di compatibilità del manifesto dell'applicazione) deve comunque fornire un percorso di codice separato per il corretto rendering a contrasto elevato in Windows 7 in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3a69a-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="3a69a-228">Se si usano le funzionalità di ComCtl32.dll versione 6, ad esempio la visualizzazione affiancata o il controllo collegamento, è necessario gestire il caso in cui tali controlli non sono disponibili nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="3a69a-229">ComCtl32.dll versione 6 non è ridistribuibile.</span><span class="sxs-lookup"><span data-stu-id="3a69a-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="3a69a-230">Testare l'applicazione per assicurarsi di non basarsi sulle funzionalità di ComCtl32.dll versione 6 senza prima verificare la versione corrente.</span><span class="sxs-lookup"><span data-stu-id="3a69a-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="3a69a-231">Non collegarsi a UxTheme.lib.</span><span class="sxs-lookup"><span data-stu-id="3a69a-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="3a69a-232">Scrivere codice di gestione degli errori per le istanze quando gli stili di visualizzazione non funzionano come previsto.</span><span class="sxs-lookup"><span data-stu-id="3a69a-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="3a69a-233">L'installazione del manifesto dell'applicazione nelle versioni precedenti non influisce sul rendering dei controlli.</span><span class="sxs-lookup"><span data-stu-id="3a69a-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a69a-234">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a69a-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a69a-235">Stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3a69a-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
