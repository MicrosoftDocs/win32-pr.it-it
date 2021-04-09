---
description: Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente per usare gli assembly affiancati disponibili da Microsoft o da altri autori affiancati di assembly.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Uso di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878974"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="92e3f-103">Uso di assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="92e3f-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="92e3f-104">Usare la procedura seguente per sviluppare una nuova applicazione o aggiornare un'applicazione esistente per usare gli [assembly affiancati](about-side-by-side-assemblies-.md) disponibili da Microsoft o da altri autori affiancati di assembly.</span><span class="sxs-lookup"><span data-stu-id="92e3f-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="92e3f-105">Per un elenco degli assembly affiancati attualmente forniti da Microsoft, vedere assembly affiancati di [Microsoft supportati](supported-microsoft-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="92e3f-106">Si noti che l'applicazione deve essere eseguita in almeno Windows XP per installare gli assembly come assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="92e3f-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="92e3f-107">Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="92e3f-108">**Per aggiungere un assembly affiancato a un'applicazione**</span><span class="sxs-lookup"><span data-stu-id="92e3f-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="92e3f-109">Identificare gli assembly affiancati richiesti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="92e3f-110">A partire da Windows XP, questi assembly affiancati e i relativi manifesti di assembly vengono installati con il sistema operativo, ma non sono registrati a livello globale.</span><span class="sxs-lookup"><span data-stu-id="92e3f-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="92e3f-111">Utilizzare un editor XML per creare un [manifesto dell'applicazione](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="92e3f-112">Vedere il manifesto dell'applicazione di esempio di seguito.</span><span class="sxs-lookup"><span data-stu-id="92e3f-112">See the example application manifest below.</span></span> <span data-ttu-id="92e3f-113">Per ulteriori informazioni, vedere [manifesti dell'applicazione](application-manifests.md) nel [riferimento ai file manifesto](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="92e3f-114">Immettere i valori degli attributi nel sottoelemento [*assemblyIdentity del contesto def*](d-sbscs-gly.md) del manifesto dell'applicazione che definisce in modo univoco l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="92e3f-115">Per ulteriori informazioni sul contesto di definizione di **assemblyIdentity**, vedere [manifesti dell'applicazione](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="92e3f-116">Se l'assembly contiene assembly dipendenti, immettere i valori degli attributi nei sottoelementi [*assemblyIdentity del contesto Ref*](r-sbscs-gly.md) corrispondenti del manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="92e3f-117">Per ulteriori informazioni sul contesto di riferimento **assemblyIdentity**, vedere [manifesti dell'applicazione](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="92e3f-118">È possibile includere il manifesto dell'applicazione nel file di intestazione eseguibile binario dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="92e3f-119">In questo caso, aggiungere anche la riga seguente al file di intestazione dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="92e3f-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="92e3f-120">\_ \_ \_ \_ Manifesto "YourApp.exe. manifest" dell'ID risorsa manifesto di CreateProcess</span><span class="sxs-lookup"><span data-stu-id="92e3f-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="92e3f-121">In alternativa, è possibile inserire un file manifesto separato nella stessa directory del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="92e3f-122">Il sistema operativo carica il manifesto dal file system prima, quindi controlla la sezione delle risorse del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="92e3f-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="92e3f-123">La versione del file system ha la precedenza.</span><span class="sxs-lookup"><span data-stu-id="92e3f-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="92e3f-124">Gli [assembly condivisi](/windows/desktop/Msi/shared-assemblies) devono essere installati usando la versione di [Windows Installer](../msi/windows-installer-portal.md) 2,0.</span><span class="sxs-lookup"><span data-stu-id="92e3f-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="92e3f-125">Creare un pacchetto di Windows Installer come descritto in [come installare gli assembly Win32 per la condivisione side-by-side in Windows XP](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="92e3f-126">Gli [assembly privati](/windows/desktop/Msi/private-assemblies) possono essere installati usando la versione di [Windows Installer](../msi/windows-installer-portal.md) 2,0.</span><span class="sxs-lookup"><span data-stu-id="92e3f-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="92e3f-127">Creare un pacchetto di Windows Installer come descritto in [come installare gli assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="92e3f-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="92e3f-128">È anche possibile usare qualsiasi altro programma di installazione per copiare un assembly privato e il relativo manifesto nella stessa cartella del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92e3f-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="92e3f-129">Testare l'applicazione per verificare i risultati.</span><span class="sxs-lookup"><span data-stu-id="92e3f-129">Test your application to ensure the results.</span></span> <span data-ttu-id="92e3f-130">Si noti che il computer di test non deve avere l'assembly affiancato registrato.</span><span class="sxs-lookup"><span data-stu-id="92e3f-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="92e3f-131">Distribuire l'applicazione o aggiornare come pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="92e3f-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="92e3f-132">Manifesto dell'applicazione di esempio</span><span class="sxs-lookup"><span data-stu-id="92e3f-132">Example Application Manifest</span></span>

<span data-ttu-id="92e3f-133">Di seguito è riportato un esempio di un manifesto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="92e3f-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
