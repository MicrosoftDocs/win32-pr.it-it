---
description: Windows Installer gli sviluppatori possono utilizzare le linee guida in questo argomento per creare Windows Installer pacchetti contenenti assembly.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Aggiunta di assembly a un pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227221"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="5de96-103">Aggiunta di assembly a un pacchetto</span><span class="sxs-lookup"><span data-stu-id="5de96-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="5de96-104">Windows Installer gli sviluppatori possono utilizzare le linee guida in questo argomento per creare Windows Installer pacchetti contenenti assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="5de96-105">Le linee guida seguenti si applicano agli assembly Win32 e agli assembly utilizzati dal Common Language Runtime del Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5de96-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="5de96-106">Un componente Windows Installer non deve contenere più di un assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="5de96-107">Tutti i file nell'assembly devono trovarsi in un singolo componente.</span><span class="sxs-lookup"><span data-stu-id="5de96-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="5de96-108">Ogni componente che contiene un assembly deve includere una voce nella tabella [MsiAssembly](msiassembly-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5de96-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="5de96-109">Il nome di Assembly Cache forte di ogni assembly deve essere creato nella tabella [MsiAssemblyName](msiassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5de96-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="5de96-110">Utilizzare la tabella del [Registro di sistema](registry-table.md) anziché la tabella della [classe](class-table.md) quando si registra l'interoperabilità COM per un assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="5de96-111">Gli assembly con lo stesso nome sicuro sono lo stesso assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="5de96-112">Quando lo stesso assembly viene installato da diverse applicazioni, i componenti che contengono l'assembly devono utilizzare lo stesso valore per ComponentId nelle tabelle dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5de96-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="5de96-113">Gli annunci di prodotto identificano gli assembly che possono essere installati e usati da applicazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="5de96-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="5de96-114">Gli annunci di prodotto non identificano gli assembly privati.</span><span class="sxs-lookup"><span data-stu-id="5de96-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="5de96-115">Aggiunta di assembly Win32</span><span class="sxs-lookup"><span data-stu-id="5de96-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="5de96-116">Usare le linee guida seguenti quando si includono assembly Win32:</span><span class="sxs-lookup"><span data-stu-id="5de96-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="5de96-117">Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene un assembly Win32 non può essere null.</span><span class="sxs-lookup"><span data-stu-id="5de96-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="5de96-118">Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene un assembly dei criteri Win32 deve essere il file manifesto.</span><span class="sxs-lookup"><span data-stu-id="5de96-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="5de96-119">Il valore del percorso di un [componente che](component-table.md) contiene un assembly Win32, che non è un assembly dei criteri, non deve essere il file manifesto o il file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="5de96-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="5de96-120">Deve essere un file diverso nell'assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="5de96-121">Aggiungere una riga alla tabella [MsiAssemblyName](msiassemblyname-table.md) per ogni coppia di nome e valore elencate nella sezione **assemblyIdentity** del manifesto dell'assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="5de96-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="5de96-122">Aggiunta di assembly utilizzati con la .NET Framework</span><span class="sxs-lookup"><span data-stu-id="5de96-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="5de96-123">Usare le linee guida seguenti quando si includono assembly usati dal Common Language Runtime del .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5de96-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="5de96-124">Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene l'assembly non deve essere null.</span><span class="sxs-lookup"><span data-stu-id="5de96-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="5de96-125">Quando si installa un assembly utilizzato dal Common Language Runtime al Global Assembly Cache, il valore nella \_ colonna applicazione file della tabella MsiAssembly deve essere null.</span><span class="sxs-lookup"><span data-stu-id="5de96-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="5de96-126">Aggiungere una riga alla tabella [MsiAssemblyName](msiassemblyname-table.md) per ogni attributo del nome sicuro dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="5de96-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="5de96-127">Tutti gli assembly devono avere gli attributi Name, Version e culture specificati nella tabella MsiAssemblyName.</span><span class="sxs-lookup"><span data-stu-id="5de96-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="5de96-128">Un attributo publicKeyToken è obbligatorio per un assembly globale.</span><span class="sxs-lookup"><span data-stu-id="5de96-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="5de96-129">La tabella seguente è un esempio della tabella MsiAssemblyName per un assembly globale per l'uso da parte del Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="5de96-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="5de96-130">Tabella MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="5de96-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="5de96-131">Componente</span><span class="sxs-lookup"><span data-stu-id="5de96-131">Component</span></span>  | <span data-ttu-id="5de96-132">Nome</span><span class="sxs-lookup"><span data-stu-id="5de96-132">Name</span></span>           | <span data-ttu-id="5de96-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5de96-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="5de96-134">ComponentA</span><span class="sxs-lookup"><span data-stu-id="5de96-134">ComponentA</span></span> | <span data-ttu-id="5de96-135">Nome</span><span class="sxs-lookup"><span data-stu-id="5de96-135">Name</span></span>           | <span data-ttu-id="5de96-136">simple</span><span class="sxs-lookup"><span data-stu-id="5de96-136">simple</span></span>           |
| <span data-ttu-id="5de96-137">ComponentA</span><span class="sxs-lookup"><span data-stu-id="5de96-137">ComponentA</span></span> | <span data-ttu-id="5de96-138">version</span><span class="sxs-lookup"><span data-stu-id="5de96-138">version</span></span>        | <span data-ttu-id="5de96-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="5de96-139">1.0.0.0</span></span>          |
| <span data-ttu-id="5de96-140">ComponentA</span><span class="sxs-lookup"><span data-stu-id="5de96-140">ComponentA</span></span> | <span data-ttu-id="5de96-141">culture</span><span class="sxs-lookup"><span data-stu-id="5de96-141">Culture</span></span>        | <span data-ttu-id="5de96-142">neutrale</span><span class="sxs-lookup"><span data-stu-id="5de96-142">neutral</span></span>          |
| <span data-ttu-id="5de96-143">ComponentA</span><span class="sxs-lookup"><span data-stu-id="5de96-143">ComponentA</span></span> | <span data-ttu-id="5de96-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="5de96-144">publicKeyToken</span></span> | <span data-ttu-id="5de96-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="5de96-145">9d1ec8380f483f5a</span></span> |



 

 

 



