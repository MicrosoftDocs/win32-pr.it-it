---
description: Se l'applicazione non ospita una DLL, un'estensione, un plug-in o un pannello di controllo, è possibile usare il metodo descritto in questa sezione per abilitare un assembly per l'applicazione.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Abilitazione di un assembly in un'applicazione senza estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318641"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="6ea19-103">Abilitazione di un assembly in un'applicazione senza estensioni</span><span class="sxs-lookup"><span data-stu-id="6ea19-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="6ea19-104">Se l'applicazione non ospita una DLL, un'estensione, un plug-in o un pannello di controllo, è possibile usare il metodo descritto in questa sezione per abilitare un assembly per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ea19-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="6ea19-105">Per ulteriori informazioni sull'aggiunta di un assembly alle applicazioni con estensioni, vedere [Abilitazione di un assembly in un'applicazione che ospita una dll, un'estensione o un pannello di controllo](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="6ea19-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="6ea19-106">**Per abilitare un assembly in un'applicazione senza componenti ospitati**</span><span class="sxs-lookup"><span data-stu-id="6ea19-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="6ea19-107">Creare un manifesto che descriva la dipendenza dell'applicazione o dell'estensione nell'assembly.</span><span class="sxs-lookup"><span data-stu-id="6ea19-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="6ea19-108">È ad esempio possibile creare il manifesto per "YourApplication" copiando il manifesto di esempio seguente e sostituendo i valori corretti per **assemblyIdentity**, **processorArchitecture** e **Description**.</span><span class="sxs-lookup"><span data-stu-id="6ea19-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="6ea19-109">Impostare il valore di **processorArchitecture** su x86 se si compila su una piattaforma a 32 bit e su ia64 se si compila su una piattaforma a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6ea19-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="6ea19-110">L'elemento **Description** contiene una descrizione dell'opzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ea19-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="6ea19-111">Per ulteriori informazioni sul formato del manifesto, vedere [manifesti dell'applicazione](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="6ea19-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="6ea19-112">Aggiungere il manifesto all'applicazione come risorsa nel file di intestazione eseguibile binario dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ea19-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="6ea19-113">Non è consigliabile aggiungere il manifesto all'applicazione come file manifesto esterno.</span><span class="sxs-lookup"><span data-stu-id="6ea19-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="6ea19-114">Per aggiungere il manifesto come risorsa, creare una risorsa nell'applicazione di tipo RT \_ manifest ID 1.</span><span class="sxs-lookup"><span data-stu-id="6ea19-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="6ea19-115">Ad esempio, se il nome dell'applicazione è YourApp, il file di intestazione dell'applicazione deve contenere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6ea19-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="6ea19-116">Se invece si aggiunge il manifesto come file manifesto esterno, assicurarsi che l'installazione copi il file manifesto nella cartella contenente il file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ea19-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="6ea19-117">Eseguire un test per assicurarsi che gli assembly usati dall'applicazione funzionino correttamente nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ea19-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



