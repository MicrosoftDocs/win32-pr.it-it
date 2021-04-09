---
description: La tabella MsiAssembly specifica le impostazioni Windows Installer per gli assembly Microsoft .NET Framework e gli assembly Win32. Per ulteriori informazioni, vedere installazione di assembly nella global assembly cache e installazione di assembly Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabella MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968587"
---
# <a name="msiassembly-table"></a><span data-ttu-id="9172e-104">Tabella MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="9172e-104">MsiAssembly Table</span></span>

<span data-ttu-id="9172e-105">La tabella MsiAssembly specifica le impostazioni Windows Installer per gli assembly Microsoft .NET Framework e gli assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="9172e-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="9172e-106">Per ulteriori informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="9172e-107">In Windows XP Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="9172e-108">Per ulteriori informazioni, vedere l' [API assembly side-by-side](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="9172e-109">**Windows 2000:** Questa funzionalità non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9172e-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="9172e-110">La tabella MsiAssembly include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="9172e-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="9172e-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="9172e-111">Column</span></span>            | <span data-ttu-id="9172e-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9172e-112">Type</span></span>                         | <span data-ttu-id="9172e-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="9172e-113">Key</span></span> | <span data-ttu-id="9172e-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="9172e-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="9172e-115">Componente\_</span><span class="sxs-lookup"><span data-stu-id="9172e-115">Component\_</span></span>       | [<span data-ttu-id="9172e-116">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9172e-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="9172e-117">S</span><span class="sxs-lookup"><span data-stu-id="9172e-117">Y</span></span>   | <span data-ttu-id="9172e-118">N</span><span class="sxs-lookup"><span data-stu-id="9172e-118">N</span></span>        |
| <span data-ttu-id="9172e-119">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="9172e-119">Feature\_</span></span>         | [<span data-ttu-id="9172e-120">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9172e-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="9172e-121">N</span><span class="sxs-lookup"><span data-stu-id="9172e-121">N</span></span>   | <span data-ttu-id="9172e-122">N</span><span class="sxs-lookup"><span data-stu-id="9172e-122">N</span></span>        |
| <span data-ttu-id="9172e-123">\_Manifesto file</span><span class="sxs-lookup"><span data-stu-id="9172e-123">File\_Manifest</span></span>    | [<span data-ttu-id="9172e-124">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9172e-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="9172e-125">N</span><span class="sxs-lookup"><span data-stu-id="9172e-125">N</span></span>   | <span data-ttu-id="9172e-126">S</span><span class="sxs-lookup"><span data-stu-id="9172e-126">Y</span></span>        |
| <span data-ttu-id="9172e-127">\_Applicazione file</span><span class="sxs-lookup"><span data-stu-id="9172e-127">File\_Application</span></span> | [<span data-ttu-id="9172e-128">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9172e-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="9172e-129">N</span><span class="sxs-lookup"><span data-stu-id="9172e-129">N</span></span>   | <span data-ttu-id="9172e-130">S</span><span class="sxs-lookup"><span data-stu-id="9172e-130">Y</span></span>        |
| <span data-ttu-id="9172e-131">Attributi</span><span class="sxs-lookup"><span data-stu-id="9172e-131">Attributes</span></span>        | [<span data-ttu-id="9172e-132">Integer</span><span class="sxs-lookup"><span data-stu-id="9172e-132">Integer</span></span>](integer.md)       | <span data-ttu-id="9172e-133">N</span><span class="sxs-lookup"><span data-stu-id="9172e-133">N</span></span>   | <span data-ttu-id="9172e-134">S</span><span class="sxs-lookup"><span data-stu-id="9172e-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9172e-135">Colonne</span><span class="sxs-lookup"><span data-stu-id="9172e-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9172e-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="9172e-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9172e-137">Chiave nella tabella dei [componenti](component-table.md) che specifica il componente Windows Installer che contiene l'assembly.</span><span class="sxs-lookup"><span data-stu-id="9172e-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="9172e-138">Il valore in questo campo non deve essere impostato su null.</span><span class="sxs-lookup"><span data-stu-id="9172e-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="9172e-139">Il campo del percorso di un componente della [tabella dei componenti](component-table.md) non può essere null.</span><span class="sxs-lookup"><span data-stu-id="9172e-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="9172e-140">Per gli assembly Win32, il percorso di un componente non può essere il file manifesto specificato nel file \_ manifesto.</span><span class="sxs-lookup"><span data-stu-id="9172e-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="9172e-141">Il manifesto può essere il percorso di un .NET Framework o un assembly dei criteri.</span><span class="sxs-lookup"><span data-stu-id="9172e-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="9172e-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="9172e-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="9172e-143">Chiave nella [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="9172e-144">Quando l'assembly deve essere installato da un'installazione di funzionalità, Windows Installer installa la funzionalità a cui fa riferimento questo campo.</span><span class="sxs-lookup"><span data-stu-id="9172e-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="9172e-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>\_Manifesto file</span><span class="sxs-lookup"><span data-stu-id="9172e-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="9172e-146">Chiave esterna nella [tabella file](file-table.md) che specifica il file che contiene il manifesto per un assembly .NET Framework o un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="9172e-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="9172e-147">Per un assembly Win32, non specificare questo file come file del percorso della chiave del componente nel campo percorso chiave della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="9172e-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>\_Applicazione file</span><span class="sxs-lookup"><span data-stu-id="9172e-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="9172e-149">Per installare l'assembly in un percorso privato, immettere il file del percorso della chiave per il componente assembly in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9172e-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="9172e-150">Si tratta del valore visualizzato nel campo del percorso della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="9172e-151">Il programma di installazione può quindi installare l'assembly nella struttura di directory del componente specificato nella [tabella directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="9172e-152">Questo campo deve essere null se l'assembly deve essere installato nel Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="9172e-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="9172e-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="9172e-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="9172e-154">Immettere un valore 1 (uno) per un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="9172e-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="9172e-155">Immettere un valore pari a 0 (zero) per un assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9172e-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="9172e-156">Se la colonna Attributes è NULL, il programma di installazione considera l'assembly come un assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9172e-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9172e-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="9172e-157">Remarks</span></span>

<span data-ttu-id="9172e-158">Se è presente almeno una voce nella tabella MsiAssembly, la [tabella InstallExecuteSequence](installexecutesequence-table.md) deve contenere l' [azione MsiPublishAssemblies](msipublishassemblies-action.md)e l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="9172e-159">Poiché non è possibile eseguire il rollback degli assembly dopo che ne è stato eseguito il commit, Windows Installer utilizza un processo di installazione in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="9172e-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="9172e-160">Le interfacce per gli assembly vengono create durante le operazioni di installazione generate dall' [azione MsiPublishAssemblies](msipublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="9172e-161">Il commit degli assembly non viene eseguito fino al completamento dell'esecuzione dell' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="9172e-162">Ciò significa che se si crea un'azione personalizzata o una risorsa che si basa sull'assembly, è necessario sequenziarla dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="9172e-163">Se, ad esempio, è necessario avviare un servizio che dipende da un assembly nella global assembly cache (GAC), è necessario pianificare l'avvio di tale servizio dopo l' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9172e-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="9172e-164">Ciò significa che non è possibile utilizzare la [tabella ServiceControl](servicecontrol-table.md) per avviare il servizio, ma è necessario utilizzare un'azione personalizzata sequenziata dopo InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="9172e-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="9172e-165">Convalida</span><span class="sxs-lookup"><span data-stu-id="9172e-165">Validation</span></span>

<dl>

[<span data-ttu-id="9172e-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="9172e-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9172e-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="9172e-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9172e-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="9172e-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9172e-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="9172e-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="9172e-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="9172e-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="9172e-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="9172e-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
