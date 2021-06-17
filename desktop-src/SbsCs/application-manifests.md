---
description: Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifesti dell'applicazione
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230243"
---
# <a name="application-manifests"></a><span data-ttu-id="984b9-103">Manifesti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="984b9-103">Application Manifests</span></span>

<span data-ttu-id="984b9-104">Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="984b9-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="984b9-105">Le versioni di questi assembly devono corrispondere a quelle utilizzate per testare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="984b9-106">I manifesti di applicazione possono inoltre contenere una descrizione dei metadati di file privati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="984b9-107">Per un elenco completo di XML Schema, vedere [Schema del file manifesto.](manifest-file-schema.md)</span><span class="sxs-lookup"><span data-stu-id="984b9-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="984b9-108">I manifesti dell'applicazione hanno gli elementi e gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="984b9-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="984b9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="984b9-109">Element</span></span>                               | <span data-ttu-id="984b9-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="984b9-110">Attributes</span></span>                | <span data-ttu-id="984b9-111">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="984b9-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="984b9-112">**Assemblea**</span><span class="sxs-lookup"><span data-stu-id="984b9-112">**assembly**</span></span>                          |                           | <span data-ttu-id="984b9-113">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-113">Yes</span></span>      |
|                                       | <span data-ttu-id="984b9-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="984b9-114">**manifestVersion**</span></span>       | <span data-ttu-id="984b9-115">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-115">Yes</span></span>      |
| <span data-ttu-id="984b9-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="984b9-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="984b9-117">No</span><span class="sxs-lookup"><span data-stu-id="984b9-117">No</span></span>       |
| <span data-ttu-id="984b9-118">**Assemblyidentity**</span><span class="sxs-lookup"><span data-stu-id="984b9-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="984b9-119">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-119">Yes</span></span>      |
|                                       | <span data-ttu-id="984b9-120">**type**</span><span class="sxs-lookup"><span data-stu-id="984b9-120">**type**</span></span>                  | <span data-ttu-id="984b9-121">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-121">Yes</span></span>      |
|                                       | <span data-ttu-id="984b9-122">**nome**</span><span class="sxs-lookup"><span data-stu-id="984b9-122">**name**</span></span>                  | <span data-ttu-id="984b9-123">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-123">Yes</span></span>      |
|                                       | <span data-ttu-id="984b9-124">**language**</span><span class="sxs-lookup"><span data-stu-id="984b9-124">**language**</span></span>              | <span data-ttu-id="984b9-125">No</span><span class="sxs-lookup"><span data-stu-id="984b9-125">No</span></span>       |
|                                       | <span data-ttu-id="984b9-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="984b9-126">**processorArchitecture**</span></span> | <span data-ttu-id="984b9-127">No</span><span class="sxs-lookup"><span data-stu-id="984b9-127">No</span></span>       |
|                                       | <span data-ttu-id="984b9-128">**version**</span><span class="sxs-lookup"><span data-stu-id="984b9-128">**version**</span></span>               | <span data-ttu-id="984b9-129">Sì</span><span class="sxs-lookup"><span data-stu-id="984b9-129">Yes</span></span>      |
|                                       | <span data-ttu-id="984b9-130">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="984b9-130">**publicKeyToken**</span></span>        | <span data-ttu-id="984b9-131">No</span><span class="sxs-lookup"><span data-stu-id="984b9-131">No</span></span>       |
| <span data-ttu-id="984b9-132">**compatibilità**</span><span class="sxs-lookup"><span data-stu-id="984b9-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="984b9-133">No</span><span class="sxs-lookup"><span data-stu-id="984b9-133">No</span></span>       |
| <span data-ttu-id="984b9-134">**applicazione**</span><span class="sxs-lookup"><span data-stu-id="984b9-134">**application**</span></span>                       |                           | <span data-ttu-id="984b9-135">No</span><span class="sxs-lookup"><span data-stu-id="984b9-135">No</span></span>       |
| <span data-ttu-id="984b9-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="984b9-136">**supportedOS**</span></span>                       | <span data-ttu-id="984b9-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="984b9-137">**Id**</span></span>                    | <span data-ttu-id="984b9-138">No</span><span class="sxs-lookup"><span data-stu-id="984b9-138">No</span></span>       |
| <span data-ttu-id="984b9-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="984b9-139">**maxversiontested**</span></span>                  | <span data-ttu-id="984b9-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="984b9-140">**Id**</span></span>                    | <span data-ttu-id="984b9-141">No</span><span class="sxs-lookup"><span data-stu-id="984b9-141">No</span></span>       |
| <span data-ttu-id="984b9-142">**Dipendenza**</span><span class="sxs-lookup"><span data-stu-id="984b9-142">**dependency**</span></span>                        |                           | <span data-ttu-id="984b9-143">No</span><span class="sxs-lookup"><span data-stu-id="984b9-143">No</span></span>       |
| <span data-ttu-id="984b9-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="984b9-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="984b9-145">No</span><span class="sxs-lookup"><span data-stu-id="984b9-145">No</span></span>       |
| <span data-ttu-id="984b9-146">**file**</span><span class="sxs-lookup"><span data-stu-id="984b9-146">**file**</span></span>                              |                           | <span data-ttu-id="984b9-147">No</span><span class="sxs-lookup"><span data-stu-id="984b9-147">No</span></span>       |
|                                       | <span data-ttu-id="984b9-148">**nome**</span><span class="sxs-lookup"><span data-stu-id="984b9-148">**name**</span></span>                  | <span data-ttu-id="984b9-149">No</span><span class="sxs-lookup"><span data-stu-id="984b9-149">No</span></span>       |
|                                       | <span data-ttu-id="984b9-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="984b9-150">**hashalg**</span></span>               | <span data-ttu-id="984b9-151">No</span><span class="sxs-lookup"><span data-stu-id="984b9-151">No</span></span>       |
|                                       | <span data-ttu-id="984b9-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="984b9-152">**hash**</span></span>                  | <span data-ttu-id="984b9-153">No</span><span class="sxs-lookup"><span data-stu-id="984b9-153">No</span></span>       |
| <span data-ttu-id="984b9-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="984b9-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="984b9-155">No</span><span class="sxs-lookup"><span data-stu-id="984b9-155">No</span></span>       |
| <span data-ttu-id="984b9-156">**autoElevate**</span><span class="sxs-lookup"><span data-stu-id="984b9-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="984b9-157">No</span><span class="sxs-lookup"><span data-stu-id="984b9-157">No</span></span>       |
| <span data-ttu-id="984b9-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="984b9-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="984b9-159">No</span><span class="sxs-lookup"><span data-stu-id="984b9-159">No</span></span>       |
| <span data-ttu-id="984b9-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="984b9-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="984b9-161">No</span><span class="sxs-lookup"><span data-stu-id="984b9-161">No</span></span>       |
| <span data-ttu-id="984b9-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="984b9-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="984b9-163">No</span><span class="sxs-lookup"><span data-stu-id="984b9-163">No</span></span>       |
| <span data-ttu-id="984b9-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="984b9-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="984b9-165">No</span><span class="sxs-lookup"><span data-stu-id="984b9-165">No</span></span>       |
| <span data-ttu-id="984b9-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="984b9-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="984b9-167">No</span><span class="sxs-lookup"><span data-stu-id="984b9-167">No</span></span>       |
| <span data-ttu-id="984b9-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="984b9-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="984b9-169">No</span><span class="sxs-lookup"><span data-stu-id="984b9-169">No</span></span>       |
| <span data-ttu-id="984b9-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="984b9-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="984b9-171">No</span><span class="sxs-lookup"><span data-stu-id="984b9-171">No</span></span>       |
| <span data-ttu-id="984b9-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="984b9-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="984b9-173">No</span><span class="sxs-lookup"><span data-stu-id="984b9-173">No</span></span>       |
| <span data-ttu-id="984b9-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="984b9-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="984b9-175">No</span><span class="sxs-lookup"><span data-stu-id="984b9-175">No</span></span>       |
| <span data-ttu-id="984b9-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="984b9-176">**msix**</span></span>                              |                           | <span data-ttu-id="984b9-177">No</span><span class="sxs-lookup"><span data-stu-id="984b9-177">No</span></span>       |
| <span data-ttu-id="984b9-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="984b9-178">**heapType**</span></span>                          |                           | <span data-ttu-id="984b9-179">No</span><span class="sxs-lookup"><span data-stu-id="984b9-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="984b9-180">Percorso file</span><span class="sxs-lookup"><span data-stu-id="984b9-180">File Location</span></span>

<span data-ttu-id="984b9-181">I manifesti dell'applicazione devono essere inclusi come risorsa nel file EXE o nella DLL dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="984b9-182">Per altre informazioni, [vedere Installazione di assembly side-by-side.](installing-side-by-side-assemblies.md)</span><span class="sxs-lookup"><span data-stu-id="984b9-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="984b9-183">Sintassi del nome file</span><span class="sxs-lookup"><span data-stu-id="984b9-183">File Name Syntax</span></span>

<span data-ttu-id="984b9-184">Il nome di un file manifesto dell'applicazione è il nome del file eseguibile dell'applicazione seguito da .manifest.</span><span class="sxs-lookup"><span data-stu-id="984b9-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="984b9-185">Ad esempio, un manifesto dell'applicazione che fa riferimento example.exe o example.dll usa la sintassi del nome file seguente.</span><span class="sxs-lookup"><span data-stu-id="984b9-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="984b9-186">È possibile omettere il campo *<'ID*> risorsa se l'ID risorsa è 1.</span><span class="sxs-lookup"><span data-stu-id="984b9-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="984b9-187">\***example.exe.<'ID risorsa\*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="984b9-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="984b9-188">\***example.dll.<'ID risorsa\*>.manifest**</span><span class="sxs-lookup"><span data-stu-id="984b9-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="984b9-189">Elementi</span><span class="sxs-lookup"><span data-stu-id="984b9-189">Elements</span></span>

<span data-ttu-id="984b9-190">Per i nomi degli elementi e degli attributi viene fatto distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="984b9-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="984b9-191">Per i valori di elementi e attributi non viene fatta distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo type.</span><span class="sxs-lookup"><span data-stu-id="984b9-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="984b9-192">assembly</span><span class="sxs-lookup"><span data-stu-id="984b9-192">assembly</span></span>

<span data-ttu-id="984b9-193">Elemento contenitore.</span><span class="sxs-lookup"><span data-stu-id="984b9-193">A container element.</span></span> <span data-ttu-id="984b9-194">Il primo sottoelemento deve essere **un elemento noInherit** **o assemblyIdentity.**</span><span class="sxs-lookup"><span data-stu-id="984b9-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="984b9-195">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="984b9-195">Required.</span></span>

<span data-ttu-id="984b9-196">**L'elemento assembly** deve essere nello spazio dei nomi "urn:schemas-microsoft-com:asm.v1".</span><span class="sxs-lookup"><span data-stu-id="984b9-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="984b9-197">Anche gli elementi figlio dell'assembly devono essere in questo spazio dei nomi, per ereditarietà o tramite l'assegnazione di tag.</span><span class="sxs-lookup"><span data-stu-id="984b9-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="984b9-198">**L'elemento assembly** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="984b9-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="984b9-199">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-199">Attribute</span></span>           | <span data-ttu-id="984b9-200">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="984b9-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="984b9-201">**manifestVersion**</span></span> | <span data-ttu-id="984b9-202">**L'attributo manifestVersion** deve essere impostato su 1.0.</span><span class="sxs-lookup"><span data-stu-id="984b9-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="984b9-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="984b9-203">noInherit</span></span>

<span data-ttu-id="984b9-204">Includere questo elemento in un manifesto dell'applicazione per impostare i [contesti di](activation-contexts.md) attivazione generati dal manifesto con il flag "no inherit".</span><span class="sxs-lookup"><span data-stu-id="984b9-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="984b9-205">Quando questo flag non è impostato in un contesto di attivazione e il contesto di attivazione è attivo, viene ereditato dai nuovi thread nello stesso processo, finestra, routine finestra e chiamate di [procedura asincrone](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="984b9-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="984b9-206">L'impostazione di questo flag impedisce al nuovo oggetto di ereditare il contesto attivo.</span><span class="sxs-lookup"><span data-stu-id="984b9-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="984b9-207">**L'elemento noInherit** è facoltativo e in genere viene omesso.</span><span class="sxs-lookup"><span data-stu-id="984b9-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="984b9-208">La maggior parte degli assembly non funziona correttamente usando un contesto di attivazione no-inherit perché l'assembly deve essere progettato in modo esplicito per gestire la propagazione del proprio contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="984b9-209">L'uso **dell'elemento noInherit** richiede che tutti gli assembly dipendenti a cui fa riferimento il manifesto dell'applicazione presentino un elemento **noInherit** nel manifesto [dell'assembly.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="984b9-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="984b9-210">Se **noInherit** viene usato in un manifesto, deve essere il primo sottoelemento **dell'elemento assembly.**</span><span class="sxs-lookup"><span data-stu-id="984b9-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="984b9-211">**L'elemento assemblyIdentity** deve essere immediatamente successivo all'elemento **noInherit.**</span><span class="sxs-lookup"><span data-stu-id="984b9-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="984b9-212">Se **non si usa noInherit,** **assemblyIdentity** deve essere il primo sottoelemento dell'elemento **assembly.**</span><span class="sxs-lookup"><span data-stu-id="984b9-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="984b9-213">**L'elemento noInherit** non ha elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="984b9-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="984b9-214">Non è un elemento valido nei [manifesti dell'assembly.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="984b9-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="984b9-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="984b9-215">assemblyIdentity</span></span>

<span data-ttu-id="984b9-216">Come primo sottoelemento di un **elemento assembly,** **assemblyIdentity** descrive e identifica in modo univoco l'applicazione proprietaria del manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="984b9-217">Come primo sottoelemento di un elemento **dependentAssembly,** **assemblyIdentity** descrive un assembly side-by-side richiesto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="984b9-218">Si noti che ogni assembly a cui viene fatto riferimento nel manifesto dell'applicazione richiede un **elemento assemblyIdentity** che corrisponda esattamente all'elemento **assemblyIdentity** nel manifesto dell'assembly a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="984b9-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="984b9-219">**L'elemento assemblyIdentity** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="984b9-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="984b9-220">Non ha sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="984b9-220">It has no subelements.</span></span>

| <span data-ttu-id="984b9-221">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-221">Attribute</span></span>                 | <span data-ttu-id="984b9-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984b9-223">**type**</span><span class="sxs-lookup"><span data-stu-id="984b9-223">**type**</span></span>                  | <span data-ttu-id="984b9-224">Specifica il tipo di applicazione o assembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="984b9-225">Il valore deve essere Win32 e tutti in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="984b9-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="984b9-226">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="984b9-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="984b9-227">**nome**</span><span class="sxs-lookup"><span data-stu-id="984b9-227">**name**</span></span>                  | <span data-ttu-id="984b9-228">Nome univoco dell'applicazione o dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="984b9-229">Usare il formato seguente per il nome: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="984b9-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="984b9-230">Ad esempio Microsoft.Windows.mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="984b9-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="984b9-231">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="984b9-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="984b9-232">**language**</span><span class="sxs-lookup"><span data-stu-id="984b9-232">**language**</span></span>              | <span data-ttu-id="984b9-233">Identifica la lingua dell'applicazione o dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="984b9-234">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-234">Optional.</span></span> <span data-ttu-id="984b9-235">Se l'applicazione o l'assembly è specifico del linguaggio, specificare il codice del linguaggio DHTML.</span><span class="sxs-lookup"><span data-stu-id="984b9-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="984b9-236">**Nell'assemblyIdentity di** un'applicazione destinata all'uso globale (indipendente dalla lingua) omettere l'attributo language.</span><span class="sxs-lookup"><span data-stu-id="984b9-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="984b9-237">In un **assemblyIdentity di** un assembly destinato all'uso globale (indipendente dalla lingua) impostare il valore della lingua su " \* ".</span><span class="sxs-lookup"><span data-stu-id="984b9-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="984b9-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="984b9-238">**processorArchitecture**</span></span> | <span data-ttu-id="984b9-239">Specifica il processore.</span><span class="sxs-lookup"><span data-stu-id="984b9-239">Specifies the processor.</span></span> <span data-ttu-id="984b9-240">I valori validi includono `x86`, `amd64`, `arm` e `arm64`.</span><span class="sxs-lookup"><span data-stu-id="984b9-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="984b9-241">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="984b9-242">**version**</span><span class="sxs-lookup"><span data-stu-id="984b9-242">**version**</span></span>               | <span data-ttu-id="984b9-243">Specifica la versione dell'applicazione o dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="984b9-244">Usare il formato di versione in quattro parti: mmmmm.nnnnn.oooooo.ppppp.</span><span class="sxs-lookup"><span data-stu-id="984b9-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="984b9-245">Ognuna delle parti separate da punti può essere compresa tra 0 e 65535 inclusi.</span><span class="sxs-lookup"><span data-stu-id="984b9-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="984b9-246">Per altre informazioni, vedere [Versioni degli assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="984b9-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="984b9-247">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="984b9-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="984b9-248">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="984b9-248">**publicKeyToken**</span></span>        | <span data-ttu-id="984b9-249">Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica con cui viene firmata l'applicazione o l'assembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="984b9-250">La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="984b9-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="984b9-251">Obbligatorio per tutti gli assembly side-by-side condivisi.</span><span class="sxs-lookup"><span data-stu-id="984b9-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="984b9-252">compatibilità</span><span class="sxs-lookup"><span data-stu-id="984b9-252">compatibility</span></span>

<span data-ttu-id="984b9-253">Contiene almeno **un'applicazione**.</span><span class="sxs-lookup"><span data-stu-id="984b9-253">Contains at least one **application**.</span></span> <span data-ttu-id="984b9-254">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-254">It has no attributes.</span></span> <span data-ttu-id="984b9-255">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-255">Optional.</span></span> <span data-ttu-id="984b9-256">Per impostazione predefinita, i manifesti dell'applicazione senza un elemento di compatibilità sono compatibili con Windows Vista in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="984b9-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="984b9-257">application</span><span class="sxs-lookup"><span data-stu-id="984b9-257">application</span></span>

<span data-ttu-id="984b9-258">Contiene almeno un **elemento supportedOS.**</span><span class="sxs-lookup"><span data-stu-id="984b9-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="984b9-259">A partire Windows 10 versione 1903, può contenere anche un elemento **maxversiontested** facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="984b9-260">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-260">It has no attributes.</span></span> <span data-ttu-id="984b9-261">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="984b9-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="984b9-262">supportedOS</span></span>

<span data-ttu-id="984b9-263">**L'elemento supportedOS** ha l'attributo seguente.</span><span class="sxs-lookup"><span data-stu-id="984b9-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="984b9-264">Non ha sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="984b9-264">It has no subelements.</span></span>

| <span data-ttu-id="984b9-265">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-265">Attribute</span></span> | <span data-ttu-id="984b9-266">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="984b9-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="984b9-267">**Id**</span></span>    | <span data-ttu-id="984b9-268">Impostare l'attributo Id su **{e2011457-1546-43c5-a5fe-008dee3d3f0}** per eseguire l'applicazione usando la funzionalità Vista.</span><span class="sxs-lookup"><span data-stu-id="984b9-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="984b9-269">In questo modo un'applicazione progettata per Windows Vista può essere eseguita in un sistema operativo successivo.</span><span class="sxs-lookup"><span data-stu-id="984b9-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="984b9-270">Impostare l'attributo Id su **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** per eseguire l'applicazione usando la funzionalità di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="984b9-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="984b9-271">Le applicazioni che supportano Windows Vista, Windows 7 e Windows 8 non richiedono manifesti separati.</span><span class="sxs-lookup"><span data-stu-id="984b9-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="984b9-272">In questo caso, aggiungere i GUID per tutti i sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="984b9-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="984b9-273">Per informazioni sul comportamento dell'attributo **Id** in Windows, vedere il Windows 8 di compatibilità di [Windows Server 2012.](https://www.microsoft.com/download/details.aspx?id=27416)</span><span class="sxs-lookup"><span data-stu-id="984b9-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="984b9-274">I GUID seguenti corrispondono ai sistemi operativi indicati:</span><span class="sxs-lookup"><span data-stu-id="984b9-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="984b9-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 e Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="984b9-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="984b9-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="984b9-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="984b9-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="984b9-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="984b9-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="984b9-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="984b9-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista e Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="984b9-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="984b9-280">È possibile testare questa funzionalità in Windows 7 o Windows 8.x eseguendo Monitoraggio risorse (resmon), andare alla scheda CPU, fare clic con il pulsante destro del mouse sulle etichette di colonna, selezionare "Seleziona colonna..." e selezionare "Contesto sistema operativo".</span><span class="sxs-lookup"><span data-stu-id="984b9-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="984b9-281">In Windows 8.x è anche possibile trovare questa colonna disponibile nel Gestione attività (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="984b9-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="984b9-282">Il contenuto della colonna mostra il valore più alto trovato o "Windows Vista" come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="984b9-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="984b9-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="984b9-283">maxversiontested</span></span>

<span data-ttu-id="984b9-284">**L'elemento maxversiontested** specifica le versioni di Windows in cui è stata testata l'applicazione a partire dalla versione minima del sistema operativo supportata dall'applicazione fino alla versione massima.</span><span class="sxs-lookup"><span data-stu-id="984b9-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="984b9-285">Il set completo di versioni è disponibile [qui.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="984b9-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="984b9-286">Deve essere usato dalle applicazioni desktop che usano isole [XAML](/windows/apps/desktop/modernize/xaml-islands) e che non sono distribuite in un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="984b9-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="984b9-287">Questo elemento è supportato in Windows 10, versione 1903 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="984b9-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="984b9-288">**L'elemento maxversiontested** ha l'attributo seguente.</span><span class="sxs-lookup"><span data-stu-id="984b9-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="984b9-289">Non ha sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="984b9-289">It has no subelements.</span></span>

| <span data-ttu-id="984b9-290">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-290">Attribute</span></span> | <span data-ttu-id="984b9-291">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="984b9-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="984b9-292">**Id**</span></span>    | <span data-ttu-id="984b9-293">Impostare l'attributo Id su una stringa di versione in 4 parti che specifica la versione massima di Windows su cui è stata testata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="984b9-294">Ad esempio, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="984b9-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="984b9-295">dependency</span><span class="sxs-lookup"><span data-stu-id="984b9-295">dependency</span></span>

<span data-ttu-id="984b9-296">Contiene almeno un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="984b9-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="984b9-297">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-297">It has no attributes.</span></span> <span data-ttu-id="984b9-298">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="984b9-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="984b9-299">dependentAssembly</span></span>

<span data-ttu-id="984b9-300">Il primo sottoelemento **di dependentAssembly** deve essere un **elemento assemblyIdentity** che descrive un assembly side-by-side richiesto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="984b9-301">Ogni **dependentAssembly deve** essere all'interno di una **sola dipendenza.**</span><span class="sxs-lookup"><span data-stu-id="984b9-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="984b9-302">Non dispone di attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="984b9-303">file</span><span class="sxs-lookup"><span data-stu-id="984b9-303">file</span></span>

<span data-ttu-id="984b9-304">Specifica i file privati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="984b9-305">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-305">Optional.</span></span>

<span data-ttu-id="984b9-306">**L'elemento file** ha gli attributi illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="984b9-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="984b9-307">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-307">Attribute</span></span>   | <span data-ttu-id="984b9-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984b9-309">**nome**</span><span class="sxs-lookup"><span data-stu-id="984b9-309">**name**</span></span>    | <span data-ttu-id="984b9-310">Nome del file.</span><span class="sxs-lookup"><span data-stu-id="984b9-310">Name of the file.</span></span> <span data-ttu-id="984b9-311">Ad esempio, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="984b9-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="984b9-312">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="984b9-312">**hashalg**</span></span> | <span data-ttu-id="984b9-313">Algoritmo utilizzato per creare un hash del file.</span><span class="sxs-lookup"><span data-stu-id="984b9-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="984b9-314">Questo valore deve essere SHA1.</span><span class="sxs-lookup"><span data-stu-id="984b9-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="984b9-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="984b9-315">**hash**</span></span>    | <span data-ttu-id="984b9-316">Hash del file a cui si fa riferimento in base al nome.</span><span class="sxs-lookup"><span data-stu-id="984b9-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="984b9-317">Stringa esadecimale di lunghezza a seconda dell'algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="984b9-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="984b9-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="984b9-318">activeCodePage</span></span>

<span data-ttu-id="984b9-319">Forzare un processo a usare UTF-8 come tabella codici del processo.</span><span class="sxs-lookup"><span data-stu-id="984b9-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="984b9-320">**activeCodePage è** stato aggiunto in Windows versione 1903 (aggiornamento di maggio 2019).</span><span class="sxs-lookup"><span data-stu-id="984b9-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="984b9-321">È possibile dichiarare questa proprietà e impostarla come destinazione/esecuzione nelle build precedenti di Windows, ma è necessario gestire il rilevamento e la conversione della tabella codici legacy come di consueto.</span><span class="sxs-lookup"><span data-stu-id="984b9-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="984b9-322">Per [informazioni dettagliate, vedere Usare la tabella codici UTF-8.](/windows/uwp/design/globalizing/use-utf8-code-page)</span><span class="sxs-lookup"><span data-stu-id="984b9-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="984b9-323">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-323">This element has no attributes.</span></span> <span data-ttu-id="984b9-324">**UTF-8** è solo un valore valido per **l'elemento activeCodePage.**</span><span class="sxs-lookup"><span data-stu-id="984b9-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="984b9-325">autoElevate</span><span class="sxs-lookup"><span data-stu-id="984b9-325">autoElevate</span></span>

<span data-ttu-id="984b9-326">Specifica se l'elevazione automatica dei privilegi è abilitata.</span><span class="sxs-lookup"><span data-stu-id="984b9-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="984b9-327">**TRUE** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="984b9-328">Non dispone di attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="984b9-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="984b9-329">disableTheming</span></span>

<span data-ttu-id="984b9-330">Specifica se l'impostazione di un tema per gli elementi dell'interfaccia utente è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="984b9-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="984b9-331">**TRUE** indica disabilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="984b9-332">Non dispone di attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="984b9-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="984b9-333">disableWindowFiltering</span></span>

<span data-ttu-id="984b9-334">Specifica se disabilitare il filtro delle finestre.</span><span class="sxs-lookup"><span data-stu-id="984b9-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="984b9-335">**TRUE** disabilita il filtro delle finestre in modo che sia possibile enumerare le finestre immersive dal desktop.</span><span class="sxs-lookup"><span data-stu-id="984b9-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="984b9-336">**disableWindowFiltering** è stato aggiunto Windows 8 e non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="984b9-337">dpiAware</span><span class="sxs-lookup"><span data-stu-id="984b9-337">dpiAware</span></span>

<span data-ttu-id="984b9-338">Specifica se il processo corrente è in grado di riconoscere i punti per pollice (dpi).</span><span class="sxs-lookup"><span data-stu-id="984b9-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="984b9-339">**Windows 10, versione 1607:** **L'elemento dpiAware** viene ignorato se è presente l'elemento **dpiAwareness.**</span><span class="sxs-lookup"><span data-stu-id="984b9-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="984b9-340">È possibile includere entrambi gli elementi in un manifesto se si vuole specificare un comportamento diverso per Windows 10 versione 1607 rispetto a una versione precedente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="984b9-341">Nella tabella seguente viene descritto il comportamento che risulta in base alla presenza dell'elemento **dpiAware** e al testo in esso contenuto.</span><span class="sxs-lookup"><span data-stu-id="984b9-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="984b9-342">Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="984b9-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="984b9-343">Stato **dell'elemento dpiAware**</span><span class="sxs-lookup"><span data-stu-id="984b9-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="984b9-344">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="984b9-345">Assente</span><span class="sxs-lookup"><span data-stu-id="984b9-345">Absent</span></span>                            | <span data-ttu-id="984b9-346">Il processo corrente non è a conoscenza di dpi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="984b9-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="984b9-347">È possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="984b9-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="984b9-348">Contiene "true"</span><span class="sxs-lookup"><span data-stu-id="984b9-348">Contains "true"</span></span>                   | <span data-ttu-id="984b9-349">Il processo corrente è in grado di riconoscere dpi di sistema.</span><span class="sxs-lookup"><span data-stu-id="984b9-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="984b9-350">Contiene "false"</span><span class="sxs-lookup"><span data-stu-id="984b9-350">Contains "false"</span></span>                  | <span data-ttu-id="984b9-351">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="984b9-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="984b9-352">**Windows 8.1 e Windows 10:** Il processo corrente non è a conoscenza di dpi e non è possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="984b9-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="984b9-353">Contiene "true/pm"</span><span class="sxs-lookup"><span data-stu-id="984b9-353">Contains "true/pm"</span></span>                | <span data-ttu-id="984b9-354">**Windows Vista, Windows 7 e Windows 8:** Il processo corrente è in grado di riconoscere dpi di sistema.</span><span class="sxs-lookup"><span data-stu-id="984b9-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="984b9-355">**Windows 8.1 e Windows 10:** Il processo corrente è in grado di riconoscere dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="984b9-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="984b9-356">Contiene "per monitor"</span><span class="sxs-lookup"><span data-stu-id="984b9-356">Contains "per monitor"</span></span>            | <span data-ttu-id="984b9-357">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="984b9-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="984b9-358">**Windows 8.1 e Windows 10:** Il processo corrente è in grado di riconoscere dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="984b9-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="984b9-359">Contiene qualsiasi altra stringa</span><span class="sxs-lookup"><span data-stu-id="984b9-359">Contains any other string</span></span>         | <span data-ttu-id="984b9-360">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è lo stesso di quando **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="984b9-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="984b9-361">**Windows 8.1 e Windows 10:** Il processo corrente non è a conoscenza di dpi e non è possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="984b9-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="984b9-362">Per altre informazioni sulle impostazioni di consapevolezza dpi, vedere [Confronto dei livelli di consapevolezza DPI.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))</span><span class="sxs-lookup"><span data-stu-id="984b9-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="984b9-363">**dpiAware** non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="984b9-364">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="984b9-364">dpiAwareness</span></span>

<span data-ttu-id="984b9-365">Specifica se il processo corrente è in grado di riconoscere i punti per pollice (dpi).</span><span class="sxs-lookup"><span data-stu-id="984b9-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="984b9-366">La versione minima del sistema operativo che supporta l'elemento **dpiAwareness** è Windows 10 versione 1607.</span><span class="sxs-lookup"><span data-stu-id="984b9-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="984b9-367">Per le versioni che supportano **l'elemento dpiAwareness,** **dpiAwareness** esegue l'override **dell'elemento dpiAware.**</span><span class="sxs-lookup"><span data-stu-id="984b9-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="984b9-368">È possibile includere entrambi gli elementi in un manifesto se si vuole specificare un comportamento diverso per Windows 10 versione 1607 rispetto a una versione precedente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="984b9-369">**L'elemento dpiAwareness** può contenere un singolo elemento o un elenco di elementi delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="984b9-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="984b9-370">Nel secondo caso, viene usato il primo elemento (più a sinistra) nell'elenco riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="984b9-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="984b9-371">In questo modo, è possibile specificare comportamenti diversi supportati nelle versioni future del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="984b9-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="984b9-372">Nella tabella seguente viene descritto il comportamento che risulta in base alla presenza dell'elemento **dpiAwareness** e al testo in esso contenuto nell'elemento riconosciuto all'estrema sinistra.</span><span class="sxs-lookup"><span data-stu-id="984b9-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="984b9-373">Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="984b9-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="984b9-374">**Stato dell'elemento dpiAwareness:**</span><span class="sxs-lookup"><span data-stu-id="984b9-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="984b9-375">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="984b9-376">L'elemento è assente</span><span class="sxs-lookup"><span data-stu-id="984b9-376">Element is absent</span></span>                       | <span data-ttu-id="984b9-377">**L'elemento dpiAware** specifica se il processo è in grado di riconoscere dpi.</span><span class="sxs-lookup"><span data-stu-id="984b9-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="984b9-378">Non contiene elementi riconosciuti</span><span class="sxs-lookup"><span data-stu-id="984b9-378">Contains no recognized items</span></span>            | <span data-ttu-id="984b9-379">Il processo corrente non è a conoscenza di dpi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="984b9-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="984b9-380">È possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="984b9-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="984b9-381">Il primo elemento riconosciuto è "system"</span><span class="sxs-lookup"><span data-stu-id="984b9-381">First recognized item is "system"</span></span>       | <span data-ttu-id="984b9-382">Il processo corrente è in grado di riconoscere dpi di sistema.</span><span class="sxs-lookup"><span data-stu-id="984b9-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="984b9-383">Il primo elemento riconosciuto è "permonitor"</span><span class="sxs-lookup"><span data-stu-id="984b9-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="984b9-384">Il processo corrente è in grado di riconoscere dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="984b9-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="984b9-385">Il primo elemento riconosciuto è "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="984b9-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="984b9-386">Il processo corrente usa il contesto di consapevolezza dpi per monitor-v2.</span><span class="sxs-lookup"><span data-stu-id="984b9-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="984b9-387">Questo elemento verrà riconosciuto solo in Windows 10 versione 1703 o successiva.</span><span class="sxs-lookup"><span data-stu-id="984b9-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="984b9-388">Il primo elemento riconosciuto è "inconsapevole"</span><span class="sxs-lookup"><span data-stu-id="984b9-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="984b9-389">Il processo corrente non è a conoscenza di dpi.</span><span class="sxs-lookup"><span data-stu-id="984b9-389">The current process is dpi unaware.</span></span> <span data-ttu-id="984b9-390">Non **è** possibile modificare questa impostazione a livello di codice chiamando la [**funzione SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**o SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="984b9-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="984b9-391">Per altre informazioni sulle impostazioni di riconoscimento dpi supportate da questo elemento, vedere [DPI \_ AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) e [DPI \_ AWARENESS \_ CONTEXT.](/windows/desktop/hidpi/dpi-awareness-context)</span><span class="sxs-lookup"><span data-stu-id="984b9-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="984b9-392">**dpiAwareness** non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="984b9-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="984b9-393">gdiScaling</span></span>

<span data-ttu-id="984b9-394">Specifica se il ridimensionamento GDI è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="984b9-395">La versione minima del sistema operativo che supporta **l'elemento gdiScaling** Windows 10 versione 1703.</span><span class="sxs-lookup"><span data-stu-id="984b9-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="984b9-396">Il framework GDI (Graphics Device Interface) può applicare il ridimensionamento DPI alle primitive e al testo in base al monitor senza aggiornamenti all'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="984b9-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="984b9-397">Ciò può essere utile per le applicazioni GDI che non vengono più aggiornate attivamente.</span><span class="sxs-lookup"><span data-stu-id="984b9-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="984b9-398">La grafica non vettoriale ( ad esempio bitmap, icone o barre degli strumenti) non può essere ridimensionata da questo elemento.</span><span class="sxs-lookup"><span data-stu-id="984b9-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="984b9-399">Inoltre, la grafica e il testo visualizzati all'interno di bitmap create dinamicamente dalle applicazioni non possono essere ridimensionati da questo elemento.</span><span class="sxs-lookup"><span data-stu-id="984b9-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="984b9-400">**TRUE** indica che questo elemento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="984b9-401">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="984b9-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="984b9-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="984b9-403">Specifica se è abilitata la funzionalità di scorrimento ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="984b9-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="984b9-404">**TRUE** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="984b9-405">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="984b9-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="984b9-406">longPathAware</span></span>

<span data-ttu-id="984b9-407">Abilita percorsi lunghi che **superano MAX_PATH** lunghezza.</span><span class="sxs-lookup"><span data-stu-id="984b9-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="984b9-408">Questo elemento è supportato in Windows 10 versione 1607 e successive.</span><span class="sxs-lookup"><span data-stu-id="984b9-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="984b9-409">Per altre informazioni, vedi [questo articolo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="984b9-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="984b9-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="984b9-410">printerDriverIsolation</span></span>

<span data-ttu-id="984b9-411">Specifica se l'isolamento del driver della stampante è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="984b9-412">**TRUE** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="984b9-413">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-413">It has no attributes.</span></span> <span data-ttu-id="984b9-414">L'isolamento del driver della stampante migliora l'affidabilità del servizio di stampa di Windows consentendo l'esecuzione dei driver della stampante in processi separati dal processo in cui viene eseguito lo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="984b9-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="984b9-415">Il supporto per l'isolamento del driver della stampante è stato avviato in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="984b9-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="984b9-416">Un'app può dichiarare l'isolamento del driver della stampante nel manifesto dell'app per isolarsi dal driver della stampante e migliorarne l'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="984b9-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="984b9-417">Ciò significa che l'app non si arresta in modo anomalo se il driver della stampante presenta un errore.</span><span class="sxs-lookup"><span data-stu-id="984b9-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="984b9-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="984b9-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="984b9-419">Specifica se è abilitata la funzionalità di scorrimento ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="984b9-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="984b9-420">**TRUE** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="984b9-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="984b9-421">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="984b9-422">msix</span><span class="sxs-lookup"><span data-stu-id="984b9-422">msix</span></span>

<span data-ttu-id="984b9-423">Specifica le informazioni sull'identità di un pacchetto MSIX di [tipo sparse](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) per l'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="984b9-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="984b9-424">Questo elemento è supportato in Windows 10, versione 2004 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="984b9-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="984b9-425">**L'elemento msix** deve essere nello spazio dei nomi `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="984b9-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="984b9-426">Ha gli attributi illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="984b9-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="984b9-427">Attributo</span><span class="sxs-lookup"><span data-stu-id="984b9-427">Attribute</span></span>   | <span data-ttu-id="984b9-428">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984b9-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="984b9-429">**Editore**</span><span class="sxs-lookup"><span data-stu-id="984b9-429">**publisher**</span></span>    | <span data-ttu-id="984b9-430">Descrive le informazioni sull'autore.</span><span class="sxs-lookup"><span data-stu-id="984b9-430">Describes the publisher information.</span></span> <span data-ttu-id="984b9-431">Questo valore deve corrispondere **all'attributo Publisher** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) nel manifesto del pacchetto di tipo sparse.</span><span class="sxs-lookup"><span data-stu-id="984b9-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="984b9-432">**Nomepacchetto**</span><span class="sxs-lookup"><span data-stu-id="984b9-432">**packageName**</span></span> | <span data-ttu-id="984b9-433">Descrive il contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="984b9-433">Describes the contents of the package.</span></span> <span data-ttu-id="984b9-434">Questo valore deve corrispondere **all'attributo Name** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) nel manifesto del pacchetto di tipo sparse.</span><span class="sxs-lookup"><span data-stu-id="984b9-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="984b9-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="984b9-435">**applicationId**</span></span>    | <span data-ttu-id="984b9-436">Identificatore univoco dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="984b9-436">The unique identifier of the application.</span></span> <span data-ttu-id="984b9-437">Questo valore deve corrispondere **all'attributo Id** nell'elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) nel manifesto del pacchetto di tipo sparse.</span><span class="sxs-lookup"><span data-stu-id="984b9-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="984b9-438">heapType</span><span class="sxs-lookup"><span data-stu-id="984b9-438">heapType</span></span>

<span data-ttu-id="984b9-439">Esegue l'override dell'implementazione dell'heap predefinita per l'uso delle [API dell'heap Win32.](../Memory/heap-functions.md)</span><span class="sxs-lookup"><span data-stu-id="984b9-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="984b9-440">Il valore **SegmentHeap** indica che verrà usato l'heap dei segmenti.</span><span class="sxs-lookup"><span data-stu-id="984b9-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="984b9-441">L'heap dei segmenti è un'implementazione moderna dell'heap che in genere ridurrà l'utilizzo complessivo della memoria.</span><span class="sxs-lookup"><span data-stu-id="984b9-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="984b9-442">Questo elemento è supportato in Windows 10 versione 2004 (build 19041) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="984b9-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="984b9-443">Tutti gli altri valori vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="984b9-443">All other values are ignored.</span></span>

<span data-ttu-id="984b9-444">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="984b9-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="984b9-445">Esempio</span><span class="sxs-lookup"><span data-stu-id="984b9-445">Example</span></span>

<span data-ttu-id="984b9-446">Di seguito è riportato un esempio di manifesto dell'applicazione per un'applicazione denominata MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="984b9-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="984b9-447">L'applicazione utilizza l'assembly side-by-side SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="984b9-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
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
