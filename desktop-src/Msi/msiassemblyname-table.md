---
description: La tabella MsiAssembly e la tabella MsiAssemblyName specificano Windows Installer impostazioni per assembly Common Language Runtime e assembly Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabella MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319008"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="8df29-103">Tabella MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="8df29-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="8df29-104">La tabella [MsiAssembly](msiassembly-table.md) e la tabella MsiAssemblyName specificano Windows Installer impostazioni per assembly Common Language Runtime e assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="8df29-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="8df29-105">Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="8df29-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="8df29-106">La tabella MsiAssemblyName specifica lo schema per gli elementi di un nome di Assembly Cache forte per un .NET Framework o un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="8df29-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="8df29-107">Il nome viene costruito accodando tutti gli elementi con la stessa chiave del componente \_ .</span><span class="sxs-lookup"><span data-stu-id="8df29-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="8df29-108">Vedere l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="8df29-108">See the following example.</span></span>

<span data-ttu-id="8df29-109">Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="8df29-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="8df29-110">Per ulteriori informazioni, vedere l' [API assembly side-by-side](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="8df29-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="8df29-111">La tabella MsiAssemblyName include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="8df29-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="8df29-112">Colonna</span><span class="sxs-lookup"><span data-stu-id="8df29-112">Column</span></span>      | <span data-ttu-id="8df29-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="8df29-113">Type</span></span>                         | <span data-ttu-id="8df29-114">Chiave</span><span class="sxs-lookup"><span data-stu-id="8df29-114">Key</span></span> | <span data-ttu-id="8df29-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="8df29-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="8df29-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="8df29-116">Component\_</span></span> | [<span data-ttu-id="8df29-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="8df29-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="8df29-118">S</span><span class="sxs-lookup"><span data-stu-id="8df29-118">Y</span></span>   | <span data-ttu-id="8df29-119">N</span><span class="sxs-lookup"><span data-stu-id="8df29-119">N</span></span>        |
| <span data-ttu-id="8df29-120">Nome</span><span class="sxs-lookup"><span data-stu-id="8df29-120">Name</span></span>        | [<span data-ttu-id="8df29-121">Text</span><span class="sxs-lookup"><span data-stu-id="8df29-121">Text</span></span>](text.md)             | <span data-ttu-id="8df29-122">S</span><span class="sxs-lookup"><span data-stu-id="8df29-122">Y</span></span>   | <span data-ttu-id="8df29-123">N</span><span class="sxs-lookup"><span data-stu-id="8df29-123">N</span></span>        |
| <span data-ttu-id="8df29-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8df29-124">Value</span></span>       | [<span data-ttu-id="8df29-125">Text</span><span class="sxs-lookup"><span data-stu-id="8df29-125">Text</span></span>](text.md)             | <span data-ttu-id="8df29-126">N</span><span class="sxs-lookup"><span data-stu-id="8df29-126">N</span></span>   | <span data-ttu-id="8df29-127">N</span><span class="sxs-lookup"><span data-stu-id="8df29-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8df29-128">Colonne</span><span class="sxs-lookup"><span data-stu-id="8df29-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8df29-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="8df29-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="8df29-130">Chiave nella [tabella dei componenti](component-table.md) che specifica il componente Windows Installer che contiene l'assembly.</span><span class="sxs-lookup"><span data-stu-id="8df29-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="8df29-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="8df29-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="8df29-132">Nome dell'attributo associato al valore specificato nella colonna valore.</span><span class="sxs-lookup"><span data-stu-id="8df29-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="8df29-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="8df29-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="8df29-134">Valore associato al nome specificato nella colonna Name.</span><span class="sxs-lookup"><span data-stu-id="8df29-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8df29-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="8df29-135">Remarks</span></span>

<span data-ttu-id="8df29-136">Le informazioni create nella tabella MsiAssemblyName devono corrispondere a quelle contenute nel file manifesto dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="8df29-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="8df29-137">Se le informazioni contenute nella tabella manifest e MsiAssemblyName non corrispondono, la rimozione dell'applicazione può lasciare l'assembly nel computer.</span><span class="sxs-lookup"><span data-stu-id="8df29-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="8df29-138">Per gli assembly Win32 è necessario che nella tabella MsiAssemblyName sia presente una riga per ognuna delle voci seguenti nel campo Nome: tipo, nome, versione, lingua, publicKeyToken e processorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="8df29-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="8df29-139">Il valore corrispondente per ogni nome può essere immesso nel campo del valore.</span><span class="sxs-lookup"><span data-stu-id="8df29-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="8df29-140">Le coppie nome-valore nella tabella MsiAssemblyName devono corrispondere agli attributi Type, Name, Version, language, publicKeyToken e processorArchitecture nel manifesto dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="8df29-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="8df29-141">Per gli assembly di Common Language Runtime privati (.NET FrameworkVersions 1,0 e 1,1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: nome, versione e impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="8df29-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="8df29-142">Il valore corrispondente per ogni nome può essere immesso nel campo del valore.</span><span class="sxs-lookup"><span data-stu-id="8df29-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="8df29-143">Per gli assembly di Common Language Runtime globali (.NET Framework versioni 1,0 e 1,1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: nome, versione, lingua e PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="8df29-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="8df29-144">Il valore corrispondente per ogni nome può essere immesso nel campo del valore.</span><span class="sxs-lookup"><span data-stu-id="8df29-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="8df29-145">Il .NET Framework versione 1,1 è la versione minima che può essere usata per eseguire un aggiornamento sul posto di un assembly di Common Language Runtime globale.</span><span class="sxs-lookup"><span data-stu-id="8df29-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="8df29-146">È possibile controllare la proprietà [**MsiNetAssemblySupport**](msinetassemblysupport.md) per la versione.</span><span class="sxs-lookup"><span data-stu-id="8df29-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="8df29-147">La tabella MsiAssemblyName deve avere anche un campo FileVersion perché questo tipo di aggiornamento dell'assembly modifica solo la versione Fileversion.</span><span class="sxs-lookup"><span data-stu-id="8df29-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="8df29-148">Per ulteriori informazioni, vedere [aggiornamento degli assembly](updating-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="8df29-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="8df29-149">Ad esempio, il manifesto dell'assembly per Componenta potrebbe avere una sezione assemblyIdentity come indicato di seguito per un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="8df29-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="8df29-150">In questo caso, popolare la tabella MsiAssemblyName come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8df29-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="8df29-151">Componente</span><span class="sxs-lookup"><span data-stu-id="8df29-151">Component</span></span>  | <span data-ttu-id="8df29-152">Nome</span><span class="sxs-lookup"><span data-stu-id="8df29-152">Name</span></span>                  | <span data-ttu-id="8df29-153">Valore</span><span class="sxs-lookup"><span data-stu-id="8df29-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="8df29-154">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-154">ComponentA</span></span> | <span data-ttu-id="8df29-155">tipo</span><span class="sxs-lookup"><span data-stu-id="8df29-155">type</span></span>                  | <span data-ttu-id="8df29-156">Win32</span><span class="sxs-lookup"><span data-stu-id="8df29-156">win32</span></span>             |
| <span data-ttu-id="8df29-157">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-157">ComponentA</span></span> | <span data-ttu-id="8df29-158">name</span><span class="sxs-lookup"><span data-stu-id="8df29-158">name</span></span>                  | <span data-ttu-id="8df29-159">MS-sxstest-semplice</span><span class="sxs-lookup"><span data-stu-id="8df29-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="8df29-160">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-160">ComponentA</span></span> | <span data-ttu-id="8df29-161">version</span><span class="sxs-lookup"><span data-stu-id="8df29-161">version</span></span>               | <span data-ttu-id="8df29-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="8df29-162">1.0.0.0</span></span>           |
| <span data-ttu-id="8df29-163">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-163">ComponentA</span></span> | <span data-ttu-id="8df29-164">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="8df29-164">language</span></span>              | <span data-ttu-id="8df29-165">en</span><span class="sxs-lookup"><span data-stu-id="8df29-165">en</span></span>                |
| <span data-ttu-id="8df29-166">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-166">ComponentA</span></span> | <span data-ttu-id="8df29-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="8df29-167">publicKeyToken</span></span>        | <span data-ttu-id="8df29-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="8df29-168">1111111111222222</span></span>  |
| <span data-ttu-id="8df29-169">ComponentA</span><span class="sxs-lookup"><span data-stu-id="8df29-169">ComponentA</span></span> | <span data-ttu-id="8df29-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8df29-170">processorArchitecture</span></span> | <span data-ttu-id="8df29-171">x86</span><span class="sxs-lookup"><span data-stu-id="8df29-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="8df29-172">Convalida</span><span class="sxs-lookup"><span data-stu-id="8df29-172">Validation</span></span>

<dl>

[<span data-ttu-id="8df29-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="8df29-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8df29-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="8df29-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8df29-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="8df29-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8df29-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="8df29-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="8df29-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="8df29-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
