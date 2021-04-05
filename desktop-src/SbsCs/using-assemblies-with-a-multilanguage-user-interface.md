---
description: Se si vuole che gli utenti dell'applicazione, o DLL principale, siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse di lingua in DLL separate di risorse satellite.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Utilizzo di assembly con un'interfaccia utente multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750946"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="e653f-103">Utilizzo di assembly con un'interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="e653f-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="e653f-104">Se si vuole che gli utenti dell'applicazione, o DLL principale, siano in grado di modificare la lingua dell'interfaccia utente, è consigliabile inserire le risorse di lingua in DLL separate di risorse satellite.</span><span class="sxs-lookup"><span data-stu-id="e653f-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="e653f-105">Per altre informazioni sull'uso delle DLL di risorse satellite, vedere [interfaccia utente multilingue (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="e653f-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="e653f-106">Ogni DLL satellite contiene le risorse per un linguaggio diverso.</span><span class="sxs-lookup"><span data-stu-id="e653f-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="e653f-107">La DLL di base può essere fornita come assembly e ognuna delle DLL satellite può essere fornita come assembly satellite distinti.</span><span class="sxs-lookup"><span data-stu-id="e653f-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="e653f-108">In questo caso, ogni assembly satellite deve avere il proprio manifesto di assembly autodescrittivo.</span><span class="sxs-lookup"><span data-stu-id="e653f-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="e653f-109">Il manifesto dell'assembly satellite non deve descrivere alcuna dipendenza da altri assembly.</span><span class="sxs-lookup"><span data-stu-id="e653f-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="e653f-110">Tutte le dipendenze degli assembly satellite negli altri assembly devono invece essere descritte nel manifesto dell'assembly principale.</span><span class="sxs-lookup"><span data-stu-id="e653f-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="e653f-111">La versione [MUI (Multilingual User Interface)](/windows/desktop/Intl/multilingual-user-interface) di Windows consente agli utenti di specificare la lingua dell'interfaccia utente in base alle proprie preferenze, purché al sistema sia stata aggiunta la lingua richiesta.</span><span class="sxs-lookup"><span data-stu-id="e653f-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="e653f-112">Un assembly di base può supportare più lingue utilizzando più assembly MUI.</span><span class="sxs-lookup"><span data-stu-id="e653f-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="e653f-113">In questo caso, ogni assembly MUI deve avere il proprio manifesto e tutte le dipendenze da altri assembly devono essere descritte solo nel manifesto dell'assembly principale.</span><span class="sxs-lookup"><span data-stu-id="e653f-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="e653f-114">Ad esempio, proseware. Sample. pop può essere un assembly side-by-side di base che dipende dall'assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="e653f-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="e653f-115">Se proseware. Sample. pop USA MUI per supportare più lingue, è possibile fornire assembly MUI distinti per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="e653f-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="e653f-116">Ogni assembly MUI deve avere un proprio manifesto che descrive questa specifica DLL di risorse satellite.</span><span class="sxs-lookup"><span data-stu-id="e653f-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="e653f-117">I manifesti dell'assembly MUI non devono includere riferimenti alle dipendenze da altri assembly.</span><span class="sxs-lookup"><span data-stu-id="e653f-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="e653f-118">Il manifesto che descrive l'assembly principale, proseware. Sample. pop, dovrebbe descrivere la dipendenza di proseware. Sample. pop nell'assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="e653f-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="e653f-119">Gli attributi dell'elemento **assemblyIdentity** di un assembly satellite sono simili a quelli del manifesto dell'assembly di base.</span><span class="sxs-lookup"><span data-stu-id="e653f-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="e653f-120">L'attributo **Name** deve corrispondere all'assembly di base con l'aggiunta di "Resources".</span><span class="sxs-lookup"><span data-stu-id="e653f-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="e653f-121">Ad esempio, se il nome è "proseware. Tools. SpellCheck. Runtime-Libraries" nell'assembly di base, il nome nell'assembly di risorse sarà "proseware. Tools. SpellCheck. Runtime-Libraries. resources".</span><span class="sxs-lookup"><span data-stu-id="e653f-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="e653f-122">L'attributo **Language** dovrebbe identificare la lingua dell'assembly di risorse.</span><span class="sxs-lookup"><span data-stu-id="e653f-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="e653f-123">L'attributo **file** deve includere l'elenco dei file che sono dll di risorse.</span><span class="sxs-lookup"><span data-stu-id="e653f-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="e653f-124">Di seguito è riportato un esempio del manifesto per l'assembly di risorse proseware. Tools. SpellCheck. Runtime-Libraries.</span><span class="sxs-lookup"><span data-stu-id="e653f-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="e653f-125">L'assembly di base descrive una dipendenza facoltativa dall'assembly di risorse.</span><span class="sxs-lookup"><span data-stu-id="e653f-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="e653f-126">In questo esempio, se un utente esegue Windows con le impostazioni locali indicate come tedesco, un'applicazione che utilizza l'assembly proseware. Tools. SpellCheck visualizzerà il testo in tedesco.</span><span class="sxs-lookup"><span data-stu-id="e653f-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
