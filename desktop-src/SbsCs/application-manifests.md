---
description: Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifesti dell'applicazione
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320229"
---
# <a name="application-manifests"></a><span data-ttu-id="102bf-103">Manifesti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="102bf-103">Application Manifests</span></span>

<span data-ttu-id="102bf-104">Un manifesto di applicazione è un file XML nel quale vengono descritti e identificati gli assembly side-by-side condivisi e privati con i quali un'applicazione deve stabilire un'associazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="102bf-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="102bf-105">Le versioni di questi assembly devono corrispondere a quelle utilizzate per testare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="102bf-106">I manifesti di applicazione possono inoltre contenere una descrizione dei metadati di file privati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="102bf-107">Per un elenco completo delle XML Schema, vedere [schema del file manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="102bf-108">I manifesti dell'applicazione hanno gli elementi e gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="102bf-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="102bf-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="102bf-109">Element</span></span>                               | <span data-ttu-id="102bf-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="102bf-110">Attributes</span></span>                | <span data-ttu-id="102bf-111">Necessario</span><span class="sxs-lookup"><span data-stu-id="102bf-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="102bf-112">**assembly**</span><span class="sxs-lookup"><span data-stu-id="102bf-112">**assembly**</span></span>                          |                           | <span data-ttu-id="102bf-113">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-113">Yes</span></span>      |
|                                       | <span data-ttu-id="102bf-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="102bf-114">**manifestVersion**</span></span>       | <span data-ttu-id="102bf-115">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-115">Yes</span></span>      |
| <span data-ttu-id="102bf-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="102bf-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="102bf-117">No</span><span class="sxs-lookup"><span data-stu-id="102bf-117">No</span></span>       |
| <span data-ttu-id="102bf-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="102bf-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="102bf-119">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-119">Yes</span></span>      |
|                                       | <span data-ttu-id="102bf-120">**type**</span><span class="sxs-lookup"><span data-stu-id="102bf-120">**type**</span></span>                  | <span data-ttu-id="102bf-121">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-121">Yes</span></span>      |
|                                       | <span data-ttu-id="102bf-122">**nome**</span><span class="sxs-lookup"><span data-stu-id="102bf-122">**name**</span></span>                  | <span data-ttu-id="102bf-123">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-123">Yes</span></span>      |
|                                       | <span data-ttu-id="102bf-124">**language**</span><span class="sxs-lookup"><span data-stu-id="102bf-124">**language**</span></span>              | <span data-ttu-id="102bf-125">No</span><span class="sxs-lookup"><span data-stu-id="102bf-125">No</span></span>       |
|                                       | <span data-ttu-id="102bf-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="102bf-126">**processorArchitecture**</span></span> | <span data-ttu-id="102bf-127">No</span><span class="sxs-lookup"><span data-stu-id="102bf-127">No</span></span>       |
|                                       | <span data-ttu-id="102bf-128">**version**</span><span class="sxs-lookup"><span data-stu-id="102bf-128">**version**</span></span>               | <span data-ttu-id="102bf-129">Sì</span><span class="sxs-lookup"><span data-stu-id="102bf-129">Yes</span></span>      |
|                                       | <span data-ttu-id="102bf-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="102bf-130">**publicKeyToken**</span></span>        | <span data-ttu-id="102bf-131">No</span><span class="sxs-lookup"><span data-stu-id="102bf-131">No</span></span>       |
| <span data-ttu-id="102bf-132">**compatibilità**</span><span class="sxs-lookup"><span data-stu-id="102bf-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="102bf-133">No</span><span class="sxs-lookup"><span data-stu-id="102bf-133">No</span></span>       |
| <span data-ttu-id="102bf-134">**applicazione**</span><span class="sxs-lookup"><span data-stu-id="102bf-134">**application**</span></span>                       |                           | <span data-ttu-id="102bf-135">No</span><span class="sxs-lookup"><span data-stu-id="102bf-135">No</span></span>       |
| <span data-ttu-id="102bf-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="102bf-136">**supportedOS**</span></span>                       | <span data-ttu-id="102bf-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="102bf-137">**Id**</span></span>                    | <span data-ttu-id="102bf-138">No</span><span class="sxs-lookup"><span data-stu-id="102bf-138">No</span></span>       |
| <span data-ttu-id="102bf-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="102bf-139">**maxversiontested**</span></span>                  | <span data-ttu-id="102bf-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="102bf-140">**Id**</span></span>                    | <span data-ttu-id="102bf-141">No</span><span class="sxs-lookup"><span data-stu-id="102bf-141">No</span></span>       |
| <span data-ttu-id="102bf-142">**dipendenza**</span><span class="sxs-lookup"><span data-stu-id="102bf-142">**dependency**</span></span>                        |                           | <span data-ttu-id="102bf-143">No</span><span class="sxs-lookup"><span data-stu-id="102bf-143">No</span></span>       |
| <span data-ttu-id="102bf-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="102bf-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="102bf-145">No</span><span class="sxs-lookup"><span data-stu-id="102bf-145">No</span></span>       |
| <span data-ttu-id="102bf-146">**file**</span><span class="sxs-lookup"><span data-stu-id="102bf-146">**file**</span></span>                              |                           | <span data-ttu-id="102bf-147">No</span><span class="sxs-lookup"><span data-stu-id="102bf-147">No</span></span>       |
|                                       | <span data-ttu-id="102bf-148">**nome**</span><span class="sxs-lookup"><span data-stu-id="102bf-148">**name**</span></span>                  | <span data-ttu-id="102bf-149">No</span><span class="sxs-lookup"><span data-stu-id="102bf-149">No</span></span>       |
|                                       | <span data-ttu-id="102bf-150">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="102bf-150">**hashalg**</span></span>               | <span data-ttu-id="102bf-151">No</span><span class="sxs-lookup"><span data-stu-id="102bf-151">No</span></span>       |
|                                       | <span data-ttu-id="102bf-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="102bf-152">**hash**</span></span>                  | <span data-ttu-id="102bf-153">No</span><span class="sxs-lookup"><span data-stu-id="102bf-153">No</span></span>       |
| <span data-ttu-id="102bf-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="102bf-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="102bf-155">No</span><span class="sxs-lookup"><span data-stu-id="102bf-155">No</span></span>       |
| <span data-ttu-id="102bf-156">**autoElevate**</span><span class="sxs-lookup"><span data-stu-id="102bf-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="102bf-157">No</span><span class="sxs-lookup"><span data-stu-id="102bf-157">No</span></span>       |
| <span data-ttu-id="102bf-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="102bf-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="102bf-159">No</span><span class="sxs-lookup"><span data-stu-id="102bf-159">No</span></span>       |
| <span data-ttu-id="102bf-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="102bf-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="102bf-161">No</span><span class="sxs-lookup"><span data-stu-id="102bf-161">No</span></span>       |
| <span data-ttu-id="102bf-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="102bf-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="102bf-163">No</span><span class="sxs-lookup"><span data-stu-id="102bf-163">No</span></span>       |
| <span data-ttu-id="102bf-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="102bf-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="102bf-165">No</span><span class="sxs-lookup"><span data-stu-id="102bf-165">No</span></span>       |
| <span data-ttu-id="102bf-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="102bf-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="102bf-167">No</span><span class="sxs-lookup"><span data-stu-id="102bf-167">No</span></span>       |
| <span data-ttu-id="102bf-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="102bf-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="102bf-169">No</span><span class="sxs-lookup"><span data-stu-id="102bf-169">No</span></span>       |
| <span data-ttu-id="102bf-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="102bf-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="102bf-171">No</span><span class="sxs-lookup"><span data-stu-id="102bf-171">No</span></span>       |
| <span data-ttu-id="102bf-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="102bf-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="102bf-173">No</span><span class="sxs-lookup"><span data-stu-id="102bf-173">No</span></span>       |
| <span data-ttu-id="102bf-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="102bf-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="102bf-175">No</span><span class="sxs-lookup"><span data-stu-id="102bf-175">No</span></span>       |
| <span data-ttu-id="102bf-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="102bf-176">**msix**</span></span>                              |                           | <span data-ttu-id="102bf-177">No</span><span class="sxs-lookup"><span data-stu-id="102bf-177">No</span></span>       |
| <span data-ttu-id="102bf-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="102bf-178">**heapType**</span></span>                          |                           | <span data-ttu-id="102bf-179">No</span><span class="sxs-lookup"><span data-stu-id="102bf-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="102bf-180">Percorso file</span><span class="sxs-lookup"><span data-stu-id="102bf-180">File Location</span></span>

<span data-ttu-id="102bf-181">I manifesti dell'applicazione devono essere inclusi come risorsa nel file EXE o nella DLL dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="102bf-182">Per ulteriori informazioni, vedere [installazione di assembly affiancati](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="102bf-183">Sintassi del nome file</span><span class="sxs-lookup"><span data-stu-id="102bf-183">File Name Syntax</span></span>

<span data-ttu-id="102bf-184">Il nome di un file manifesto dell'applicazione è il nome dell'eseguibile dell'applicazione seguito da. manifest.</span><span class="sxs-lookup"><span data-stu-id="102bf-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="102bf-185">Ad esempio, un manifesto dell'applicazione che fa riferimento a example.exe o example.dll utilizzerebbe la sintassi del nome file seguente.</span><span class="sxs-lookup"><span data-stu-id="102bf-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="102bf-186">Se l'ID risorsa è 1, è possibile omettere l' *ID risorsa* <> campo.</span><span class="sxs-lookup"><span data-stu-id="102bf-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="102bf-187">**example.exe. <*ID risorsa*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="102bf-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="102bf-188">**example.dll. <*ID risorsa*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="102bf-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="102bf-189">Elementi</span><span class="sxs-lookup"><span data-stu-id="102bf-189">Elements</span></span>

<span data-ttu-id="102bf-190">I nomi degli elementi e degli attributi distinguono tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="102bf-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="102bf-191">I valori degli elementi e degli attributi non fanno distinzione tra maiuscole e minuscole, ad eccezione del valore dell'attributo Type.</span><span class="sxs-lookup"><span data-stu-id="102bf-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="102bf-192">assembly</span><span class="sxs-lookup"><span data-stu-id="102bf-192">assembly</span></span>

<span data-ttu-id="102bf-193">Elemento contenitore.</span><span class="sxs-lookup"><span data-stu-id="102bf-193">A container element.</span></span> <span data-ttu-id="102bf-194">Il primo sottoelemento deve essere un elemento **NoInherit** o **assemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="102bf-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="102bf-195">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="102bf-195">Required.</span></span>

<span data-ttu-id="102bf-196">L'elemento **assembly** deve trovarsi nello spazio dei nomi "urn: schemas-microsoft-com: ASM. V1".</span><span class="sxs-lookup"><span data-stu-id="102bf-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="102bf-197">Gli elementi figlio dell'assembly devono trovarsi anche in questo spazio dei nomi, in base all'ereditarietà o all'assegnazione di tag.</span><span class="sxs-lookup"><span data-stu-id="102bf-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="102bf-198">L'elemento **assembly** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="102bf-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="102bf-199">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-199">Attribute</span></span>           | <span data-ttu-id="102bf-200">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="102bf-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="102bf-201">**manifestVersion**</span></span> | <span data-ttu-id="102bf-202">L'attributo **manifestVersion** deve essere impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="102bf-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="102bf-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="102bf-203">noInherit</span></span>

<span data-ttu-id="102bf-204">Includere questo elemento in un manifesto dell'applicazione per impostare i [contesti di attivazione](activation-contexts.md) generati dal manifesto con il flag "No inherit".</span><span class="sxs-lookup"><span data-stu-id="102bf-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="102bf-205">Quando questo flag non è impostato in un contesto di attivazione e il contesto di attivazione è attivo, viene ereditato da nuovi thread nello stesso processo, Windows, le routine della finestra e le [chiamate di procedure asincrone](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="102bf-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="102bf-206">L'impostazione di questo flag impedisce al nuovo oggetto di ereditare il contesto attivo.</span><span class="sxs-lookup"><span data-stu-id="102bf-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="102bf-207">L'elemento **NoInherit** è facoltativo e in genere omesso.</span><span class="sxs-lookup"><span data-stu-id="102bf-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="102bf-208">La maggior parte degli assembly non funziona correttamente usando un contesto di attivazione senza ereditarietà perché l'assembly deve essere progettato in modo esplicito per gestire la propagazione del proprio contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="102bf-209">Per l'utilizzo dell'elemento **NoInherit** è necessario che tutti gli assembly dipendenti a cui fa riferimento il manifesto dell'applicazione dispongano di un elemento **NoInherit** nel [manifesto dell'assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="102bf-210">Se si utilizza **NoInherit** in un manifesto, deve essere il primo sottoelemento dell'elemento **assembly** .</span><span class="sxs-lookup"><span data-stu-id="102bf-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="102bf-211">L'elemento **assemblyIdentity** dovrebbe essere immediatamente successivo all'elemento **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="102bf-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="102bf-212">Se non si utilizza **NoInherit** , **assemblyIdentity** deve essere il primo sottoelemento dell'elemento **assembly** .</span><span class="sxs-lookup"><span data-stu-id="102bf-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="102bf-213">L'elemento **NoInherit** non ha elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="102bf-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="102bf-214">Non è un elemento valido nei [manifesti dell'assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="102bf-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="102bf-215">assemblyIdentity</span></span>

<span data-ttu-id="102bf-216">Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive e identifica in modo univoco l'applicazione proprietaria del manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="102bf-217">Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive un assembly side-by-side richiesto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="102bf-218">Si noti che per ogni assembly a cui viene fatto riferimento nel manifesto dell'applicazione è necessario un **assemblyIdentity** che corrisponda esattamente a **assemblyIdentity** nel manifesto dell'assembly a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="102bf-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="102bf-219">L'elemento **assemblyIdentity** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="102bf-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="102bf-220">Non contiene sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="102bf-220">It has no subelements.</span></span>

| <span data-ttu-id="102bf-221">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-221">Attribute</span></span>                 | <span data-ttu-id="102bf-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102bf-223">**type**</span><span class="sxs-lookup"><span data-stu-id="102bf-223">**type**</span></span>                  | <span data-ttu-id="102bf-224">Specifica il tipo di applicazione o di assembly.</span><span class="sxs-lookup"><span data-stu-id="102bf-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="102bf-225">Il valore deve essere Win32 e tutti in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="102bf-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="102bf-226">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="102bf-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="102bf-227">**nome**</span><span class="sxs-lookup"><span data-stu-id="102bf-227">**name**</span></span>                  | <span data-ttu-id="102bf-228">Assegna un nome univoco all'applicazione o all'assembly.</span><span class="sxs-lookup"><span data-stu-id="102bf-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="102bf-229">Usare il formato seguente per il nome: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="102bf-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="102bf-230">Ad esempio Microsoft. Windows. mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="102bf-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="102bf-231">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="102bf-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="102bf-232">**language**</span><span class="sxs-lookup"><span data-stu-id="102bf-232">**language**</span></span>              | <span data-ttu-id="102bf-233">Identifica la lingua dell'applicazione o dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="102bf-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="102bf-234">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-234">Optional.</span></span> <span data-ttu-id="102bf-235">Se l'applicazione o l'assembly è specifico della lingua, specificare il codice della lingua DHTML.</span><span class="sxs-lookup"><span data-stu-id="102bf-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="102bf-236">In **assemblyIdentity** di un'applicazione destinata all'uso in tutto il mondo (indipendente dal linguaggio) omettere l'attributo Language.</span><span class="sxs-lookup"><span data-stu-id="102bf-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="102bf-237">In un oggetto **assemblyIdentity** di un assembly progettato per l'uso in tutto il mondo (indipendente dal linguaggio) impostare il valore della lingua su " \* ".</span><span class="sxs-lookup"><span data-stu-id="102bf-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="102bf-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="102bf-238">**processorArchitecture**</span></span> | <span data-ttu-id="102bf-239">Specifica il processore.</span><span class="sxs-lookup"><span data-stu-id="102bf-239">Specifies the processor.</span></span> <span data-ttu-id="102bf-240">I valori validi includono `x86`, `amd64`, `arm` e `arm64`.</span><span class="sxs-lookup"><span data-stu-id="102bf-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="102bf-241">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="102bf-242">**version**</span><span class="sxs-lookup"><span data-stu-id="102bf-242">**version**</span></span>               | <span data-ttu-id="102bf-243">Specifica la versione dell'applicazione o dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="102bf-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="102bf-244">Usare il formato di versione in quattro parti: mmmm. NNNNN. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="102bf-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="102bf-245">Ognuna delle parti separate da punti può essere 0-65535 inclusi.</span><span class="sxs-lookup"><span data-stu-id="102bf-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="102bf-246">Per altre informazioni, vedere [versioni degli assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="102bf-247">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="102bf-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="102bf-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="102bf-248">**publicKeyToken**</span></span>        | <span data-ttu-id="102bf-249">Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui l'applicazione o l'assembly è firmato.</span><span class="sxs-lookup"><span data-stu-id="102bf-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="102bf-250">La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="102bf-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="102bf-251">Obbligatorio per tutti gli assembly affiancati condivisi.</span><span class="sxs-lookup"><span data-stu-id="102bf-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="102bf-252">compatibilità</span><span class="sxs-lookup"><span data-stu-id="102bf-252">compatibility</span></span>

<span data-ttu-id="102bf-253">Contiene almeno un' **applicazione**.</span><span class="sxs-lookup"><span data-stu-id="102bf-253">Contains at least one **application**.</span></span> <span data-ttu-id="102bf-254">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-254">It has no attributes.</span></span> <span data-ttu-id="102bf-255">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-255">Optional.</span></span> <span data-ttu-id="102bf-256">I manifesti dell'applicazione senza un elemento di compatibilità vengono predefiniti per la compatibilità con Windows Vista in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="102bf-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="102bf-257">application</span><span class="sxs-lookup"><span data-stu-id="102bf-257">application</span></span>

<span data-ttu-id="102bf-258">Contiene almeno un elemento **supported** .</span><span class="sxs-lookup"><span data-stu-id="102bf-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="102bf-259">A partire da Windows 10, versione 1903, può contenere anche un elemento facoltativo **maxversiontested** .</span><span class="sxs-lookup"><span data-stu-id="102bf-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="102bf-260">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-260">It has no attributes.</span></span> <span data-ttu-id="102bf-261">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="102bf-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="102bf-262">supportedOS</span></span>

<span data-ttu-id="102bf-263">L'elemento **supportos** presenta l'attributo seguente.</span><span class="sxs-lookup"><span data-stu-id="102bf-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="102bf-264">Non contiene sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="102bf-264">It has no subelements.</span></span>

| <span data-ttu-id="102bf-265">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-265">Attribute</span></span> | <span data-ttu-id="102bf-266">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="102bf-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="102bf-267">**Id**</span></span>    | <span data-ttu-id="102bf-268">Impostare l'attributo ID su **{e2011457-1546-43C5-a5fe-008deee3d3f0}** per eseguire l'applicazione con la funzionalità vista.</span><span class="sxs-lookup"><span data-stu-id="102bf-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="102bf-269">Ciò può consentire l'esecuzione di un'applicazione progettata per Windows Vista in un sistema operativo successivo.</span><span class="sxs-lookup"><span data-stu-id="102bf-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="102bf-270">Impostare l'attributo ID su **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** per eseguire l'applicazione utilizzando la funzionalità di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="102bf-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="102bf-271">Le applicazioni che supportano le funzionalità di Windows Vista, Windows 7 e Windows 8 non richiedono manifesti distinti.</span><span class="sxs-lookup"><span data-stu-id="102bf-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="102bf-272">In questo caso, aggiungere i GUID per tutti i sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="102bf-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="102bf-273">Per informazioni sul comportamento dell'attributo **ID** in Windows, vedere la Guida di riferimento per la compatibilità con Windows [8 e Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="102bf-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="102bf-274">I GUID seguenti corrispondono ai sistemi operativi indicati:</span><span class="sxs-lookup"><span data-stu-id="102bf-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="102bf-275">**{8e0f7a12-bfb3-4fe8-B9A5-48fd50a15a9a}** -> Windows 10, windows server 2016 e windows server 2019</span><span class="sxs-lookup"><span data-stu-id="102bf-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="102bf-276">**{1f676c76-80E1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="102bf-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="102bf-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="102bf-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="102bf-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="102bf-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="102bf-279">**{e2011457-1546-43C5-a5fe-008deee3d3f0}** -> Windows Vista e windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="102bf-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="102bf-280">Per eseguire il test in Windows 7 o Windows 8. x, è possibile eseguire Monitoraggio risorse (resmon), passare alla scheda CPU, fare clic con il pulsante destro del mouse sulle etichette delle colonne, scegliere "Seleziona colonna..." e selezionare "contesto del sistema operativo".</span><span class="sxs-lookup"><span data-stu-id="102bf-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="102bf-281">In Windows 8. x, è possibile trovare anche questa colonna disponibile in Gestione attività (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="102bf-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="102bf-282">Il contenuto della colonna Mostra il valore più alto trovato o "Windows Vista" come predefinito.</span><span class="sxs-lookup"><span data-stu-id="102bf-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="102bf-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="102bf-283">maxversiontested</span></span>

<span data-ttu-id="102bf-284">L'elemento **maxversiontested** specifica la versione massima di Windows in base alla quale l'applicazione è stata testata.</span><span class="sxs-lookup"><span data-stu-id="102bf-284">The **maxversiontested** element specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="102bf-285">Questa operazione deve essere usata da applicazioni desktop che usano le [isole XAML](/windows/apps/desktop/modernize/xaml-islands) e che non sono distribuite in un pacchetto MSIX.</span><span class="sxs-lookup"><span data-stu-id="102bf-285">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="102bf-286">Questo elemento è supportato in Windows 10, versione 1903 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="102bf-286">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="102bf-287">L'elemento **maxversiontested** ha l'attributo seguente.</span><span class="sxs-lookup"><span data-stu-id="102bf-287">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="102bf-288">Non contiene sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="102bf-288">It has no subelements.</span></span>

| <span data-ttu-id="102bf-289">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-289">Attribute</span></span> | <span data-ttu-id="102bf-290">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-290">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="102bf-291">**Id**</span><span class="sxs-lookup"><span data-stu-id="102bf-291">**Id**</span></span>    | <span data-ttu-id="102bf-292">Impostare l'attributo ID su una stringa di versione in 4 parti che specifichi la versione massima di Windows su cui è stata testata l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-292">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="102bf-293">Ad esempio, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="102bf-293">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="102bf-294">dependency</span><span class="sxs-lookup"><span data-stu-id="102bf-294">dependency</span></span>

<span data-ttu-id="102bf-295">Contiene almeno un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="102bf-295">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="102bf-296">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-296">It has no attributes.</span></span> <span data-ttu-id="102bf-297">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-297">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="102bf-298">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="102bf-298">dependentAssembly</span></span>

<span data-ttu-id="102bf-299">Il primo sottoelemento di **dependentAssembly** deve essere un elemento **assemblyIdentity** che descrive un assembly affiancato richiesto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-299">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="102bf-300">Ogni **dependentAssembly** deve trovarsi all'interno di una sola **dipendenza**.</span><span class="sxs-lookup"><span data-stu-id="102bf-300">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="102bf-301">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-301">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="102bf-302">file</span><span class="sxs-lookup"><span data-stu-id="102bf-302">file</span></span>

<span data-ttu-id="102bf-303">Specifica i file privati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-303">Specifies files that are private to the application.</span></span> <span data-ttu-id="102bf-304">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-304">Optional.</span></span>

<span data-ttu-id="102bf-305">L'elemento **file** ha gli attributi mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="102bf-305">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="102bf-306">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-306">Attribute</span></span>   | <span data-ttu-id="102bf-307">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-307">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102bf-308">**nome**</span><span class="sxs-lookup"><span data-stu-id="102bf-308">**name**</span></span>    | <span data-ttu-id="102bf-309">Nome del file.</span><span class="sxs-lookup"><span data-stu-id="102bf-309">Name of the file.</span></span> <span data-ttu-id="102bf-310">Ad esempio, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="102bf-310">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="102bf-311">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="102bf-311">**hashalg**</span></span> | <span data-ttu-id="102bf-312">Algoritmo utilizzato per creare un hash del file.</span><span class="sxs-lookup"><span data-stu-id="102bf-312">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="102bf-313">Questo valore deve essere SHA1.</span><span class="sxs-lookup"><span data-stu-id="102bf-313">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="102bf-314">**hash**</span><span class="sxs-lookup"><span data-stu-id="102bf-314">**hash**</span></span>    | <span data-ttu-id="102bf-315">Hash del file a cui si fa riferimento in base al nome.</span><span class="sxs-lookup"><span data-stu-id="102bf-315">A hash of the file referred to by name.</span></span> <span data-ttu-id="102bf-316">Stringa esadecimale di lunghezza, a seconda dell'algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="102bf-316">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="102bf-317">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="102bf-317">activeCodePage</span></span>

<span data-ttu-id="102bf-318">Forzare un processo a usare UTF-8 come tabella codici del processo.</span><span class="sxs-lookup"><span data-stu-id="102bf-318">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="102bf-319">**activeCodePage** è stato aggiunto in Windows versione 1903 (aggiornamento di maggio 2019).</span><span class="sxs-lookup"><span data-stu-id="102bf-319">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="102bf-320">È possibile dichiarare questa proprietà e la destinazione/esecuzione nelle compilazioni precedenti di Windows, ma è necessario gestire il rilevamento e la conversione della tabella codici legacy come di consueto.</span><span class="sxs-lookup"><span data-stu-id="102bf-320">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="102bf-321">Per informazioni dettagliate, vedere [usare la tabella codici UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .</span><span class="sxs-lookup"><span data-stu-id="102bf-321">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="102bf-322">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-322">This element has no attributes.</span></span> <span data-ttu-id="102bf-323">**UTF-8** è un valore valido solo per l'elemento **activeCodePage** .</span><span class="sxs-lookup"><span data-stu-id="102bf-323">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

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

### <a name="autoelevate"></a><span data-ttu-id="102bf-324">autoElevate</span><span class="sxs-lookup"><span data-stu-id="102bf-324">autoElevate</span></span>

<span data-ttu-id="102bf-325">Specifica se l'elevazione automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="102bf-325">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="102bf-326">**True** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-326">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="102bf-327">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-327">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="102bf-328">disableTheming</span><span class="sxs-lookup"><span data-stu-id="102bf-328">disableTheming</span></span>

<span data-ttu-id="102bf-329">Specifica se assegnare elementi dell'interfaccia utente un tema è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-329">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="102bf-330">**True** indica disabilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-330">**TRUE** indicates disabled.</span></span> <span data-ttu-id="102bf-331">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-331">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="102bf-332">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="102bf-332">disableWindowFiltering</span></span>

<span data-ttu-id="102bf-333">Specifica se disabilitare il filtro della finestra.</span><span class="sxs-lookup"><span data-stu-id="102bf-333">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="102bf-334">**True** Disabilita il filtro della finestra in modo che sia possibile enumerare le finestre immersive dal desktop.</span><span class="sxs-lookup"><span data-stu-id="102bf-334">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="102bf-335">**disableWindowFiltering** è stato aggiunto in Windows 8 e non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-335">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

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

### <a name="dpiaware"></a><span data-ttu-id="102bf-336">dpiAware</span><span class="sxs-lookup"><span data-stu-id="102bf-336">dpiAware</span></span>

<span data-ttu-id="102bf-337">Specifica se il processo corrente è in grado di riconoscere punti per pollice (dpi).</span><span class="sxs-lookup"><span data-stu-id="102bf-337">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="102bf-338">**Windows 10, versione 1607:** L'elemento **dpiAware** viene ignorato se è presente l'elemento **dpiAwareness** .</span><span class="sxs-lookup"><span data-stu-id="102bf-338">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="102bf-339">È possibile includere entrambi gli elementi in un manifesto se si desidera specificare un comportamento diverso per Windows 10, versione 1607, rispetto a una versione precedente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-339">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="102bf-340">Nella tabella seguente viene descritto il comportamento che si basa sulla presenza dell'elemento **dpiAware** e sul testo in essa contenuto.</span><span class="sxs-lookup"><span data-stu-id="102bf-340">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="102bf-341">Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="102bf-341">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="102bf-342">Stato dell'elemento **dpiAware**</span><span class="sxs-lookup"><span data-stu-id="102bf-342">State of the **dpiAware** element</span></span> | <span data-ttu-id="102bf-343">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-343">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="102bf-344">Assente</span><span class="sxs-lookup"><span data-stu-id="102bf-344">Absent</span></span>                            | <span data-ttu-id="102bf-345">Per impostazione predefinita, il processo corrente è a conoscenza di dpi.</span><span class="sxs-lookup"><span data-stu-id="102bf-345">The current process is dpi unaware by default.</span></span> <span data-ttu-id="102bf-346">È possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="102bf-346">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="102bf-347">Contiene "true"</span><span class="sxs-lookup"><span data-stu-id="102bf-347">Contains "true"</span></span>                   | <span data-ttu-id="102bf-348">Il processo corrente è compatibile con i valori dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="102bf-348">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="102bf-349">Contiene "false"</span><span class="sxs-lookup"><span data-stu-id="102bf-349">Contains "false"</span></span>                  | <span data-ttu-id="102bf-350">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="102bf-350">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="102bf-351">**Windows 8.1 e Windows 10:** Il processo corrente è a conoscenza di dpi e non è possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="102bf-351">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="102bf-352">Contiene "true/PM"</span><span class="sxs-lookup"><span data-stu-id="102bf-352">Contains "true/pm"</span></span>                | <span data-ttu-id="102bf-353">**Windows Vista, Windows 7 e Windows 8:** Il processo corrente è compatibile con i valori dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="102bf-353">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="102bf-354">**Windows 8.1 e Windows 10:** Il processo corrente è compatibile con i valori dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="102bf-354">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="102bf-355">Contiene "per monitoraggio"</span><span class="sxs-lookup"><span data-stu-id="102bf-355">Contains "per monitor"</span></span>            | <span data-ttu-id="102bf-356">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="102bf-356">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="102bf-357">**Windows 8.1 e Windows 10:** Il processo corrente è compatibile con i valori dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="102bf-357">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="102bf-358">Contiene qualsiasi altra stringa</span><span class="sxs-lookup"><span data-stu-id="102bf-358">Contains any other string</span></span>         | <span data-ttu-id="102bf-359">**Windows Vista, Windows 7 e Windows 8:** Il comportamento è identico a quello in cui **dpiAware** è assente.</span><span class="sxs-lookup"><span data-stu-id="102bf-359">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="102bf-360">**Windows 8.1 e Windows 10:** Il processo corrente è a conoscenza di dpi e non è possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="102bf-360">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="102bf-361">Per ulteriori informazioni sulle impostazioni di compatibilità dpi, vedere [confronto tra i livelli di riconoscimento dpi](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="102bf-361">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="102bf-362">**dpiAware** non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-362">**dpiAware** has no attributes.</span></span>

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

### <a name="dpiawareness"></a><span data-ttu-id="102bf-363">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="102bf-363">dpiAwareness</span></span>

<span data-ttu-id="102bf-364">Specifica se il processo corrente è in grado di riconoscere punti per pollice (dpi).</span><span class="sxs-lookup"><span data-stu-id="102bf-364">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="102bf-365">La versione minima del sistema operativo che supporta l'elemento **dpiAwareness** è Windows 10, versione 1607.</span><span class="sxs-lookup"><span data-stu-id="102bf-365">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="102bf-366">Per le versioni che supportano l'elemento **dpiAwareness** , **dpiAwareness** esegue l'override dell'elemento **dpiAware** .</span><span class="sxs-lookup"><span data-stu-id="102bf-366">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="102bf-367">È possibile includere entrambi gli elementi in un manifesto se si desidera specificare un comportamento diverso per Windows 10, versione 1607, rispetto a una versione precedente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-367">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="102bf-368">L'elemento **dpiAwareness** può contenere un singolo elemento o un elenco di elementi separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="102bf-368">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="102bf-369">Nel secondo caso, viene utilizzato il primo elemento (a sinistra) nell'elenco riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="102bf-369">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="102bf-370">In questo modo, è possibile specificare comportamenti diversi supportati nelle versioni future del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="102bf-370">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="102bf-371">Nella tabella seguente viene descritto il comportamento che si basa sulla presenza dell'elemento **dpiAwareness** e sul testo contenuto nell'elemento riconosciuto più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="102bf-371">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="102bf-372">Il testo all'interno dell'elemento non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="102bf-372">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="102bf-373">stato elemento **dpiAwareness** :</span><span class="sxs-lookup"><span data-stu-id="102bf-373">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="102bf-374">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-374">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="102bf-375">Elemento assente</span><span class="sxs-lookup"><span data-stu-id="102bf-375">Element is absent</span></span>                       | <span data-ttu-id="102bf-376">L'elemento **dpiAware** specifica se il processo è compatibile con dpi.</span><span class="sxs-lookup"><span data-stu-id="102bf-376">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="102bf-377">Non contiene elementi riconosciuti</span><span class="sxs-lookup"><span data-stu-id="102bf-377">Contains no recognized items</span></span>            | <span data-ttu-id="102bf-378">Per impostazione predefinita, il processo corrente è a conoscenza di dpi.</span><span class="sxs-lookup"><span data-stu-id="102bf-378">The current process is dpi unaware by default.</span></span> <span data-ttu-id="102bf-379">È possibile modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="102bf-379">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="102bf-380">Il primo elemento riconosciuto è "System"</span><span class="sxs-lookup"><span data-stu-id="102bf-380">First recognized item is "system"</span></span>       | <span data-ttu-id="102bf-381">Il processo corrente è compatibile con i valori dpi del sistema.</span><span class="sxs-lookup"><span data-stu-id="102bf-381">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="102bf-382">Il primo elemento riconosciuto è "permonitor"</span><span class="sxs-lookup"><span data-stu-id="102bf-382">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="102bf-383">Il processo corrente è compatibile con i valori dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="102bf-383">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="102bf-384">Il primo elemento riconosciuto è "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="102bf-384">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="102bf-385">Il processo corrente usa il contesto di riconoscimento dpi per monitor-V2.</span><span class="sxs-lookup"><span data-stu-id="102bf-385">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="102bf-386">Questo elemento verrà riconosciuto solo in Windows 10 versione 1703 o successiva.</span><span class="sxs-lookup"><span data-stu-id="102bf-386">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="102bf-387">Il primo elemento riconosciuto è "ignaro"</span><span class="sxs-lookup"><span data-stu-id="102bf-387">First recognized item is "unaware"</span></span>      | <span data-ttu-id="102bf-388">Il processo corrente è a conoscenza di dpi.</span><span class="sxs-lookup"><span data-stu-id="102bf-388">The current process is dpi unaware.</span></span> <span data-ttu-id="102bf-389">**Non è possibile** modificare a livello di codice questa impostazione chiamando la funzione [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) o [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="102bf-389">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="102bf-390">Per ulteriori informazioni sulle impostazioni di riconoscimento dpi supportate da questo elemento, vedere [dpi \_ Awareness](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [dpi \_ Awareness \_ context](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="102bf-390">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="102bf-391">**dpiAwareness** non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-391">**dpiAwareness** has no attributes.</span></span>

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

### <a name="gdiscaling"></a><span data-ttu-id="102bf-392">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="102bf-392">gdiScaling</span></span>

<span data-ttu-id="102bf-393">Specifica se è abilitata la scalabilità GDI.</span><span class="sxs-lookup"><span data-stu-id="102bf-393">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="102bf-394">La versione minima del sistema operativo che supporta l'elemento **gdiScaling** è Windows 10 versione 1703.</span><span class="sxs-lookup"><span data-stu-id="102bf-394">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="102bf-395">Il Framework GDI (Graphics Device Interface) può applicare la scalabilità DPI alle primitive e al testo in base al monitoraggio senza aggiornamenti per l'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="102bf-395">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="102bf-396">Questa operazione può essere utile per le applicazioni GDI che non sono più attivamente aggiornate.</span><span class="sxs-lookup"><span data-stu-id="102bf-396">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="102bf-397">L'elemento non può ridimensionare elementi grafici non vettoriali, ad esempio bitmap, icone o barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="102bf-397">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="102bf-398">Inoltre, la grafica e il testo visualizzati all'interno di bitmap costruite dinamicamente dalle applicazioni non possono essere ridimensionati in base a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="102bf-398">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="102bf-399">**True** indica che questo elemento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-399">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="102bf-400">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-400">It has no attributes.</span></span>


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

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="102bf-401">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="102bf-401">highResolutionScrollingAware</span></span>

<span data-ttu-id="102bf-402">Specifica se è abilitata la funzionalità di scorrimento a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="102bf-402">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="102bf-403">**True** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-403">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="102bf-404">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-404">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="102bf-405">longPathAware</span><span class="sxs-lookup"><span data-stu-id="102bf-405">longPathAware</span></span>

<span data-ttu-id="102bf-406">Abilita percorsi lunghi che superano **MAX_PATH** lunghezza.</span><span class="sxs-lookup"><span data-stu-id="102bf-406">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="102bf-407">Questo elemento è supportato in Windows 10, versione 1607 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="102bf-407">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="102bf-408">Per altre informazioni, vedi [questo articolo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="102bf-408">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

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

### <a name="printerdriverisolation"></a><span data-ttu-id="102bf-409">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="102bf-409">printerDriverIsolation</span></span>

<span data-ttu-id="102bf-410">Specifica se l'isolamento del driver della stampante è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-410">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="102bf-411">**True** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-411">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="102bf-412">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-412">It has no attributes.</span></span> <span data-ttu-id="102bf-413">L'isolamento dei driver della stampante migliora l'affidabilità del servizio di stampa Windows consentendo ai driver della stampante di essere eseguiti in processi distinti dal processo in cui viene eseguito lo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="102bf-413">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="102bf-414">Supporto per l'isolamento dei driver della stampante avviato in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="102bf-414">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="102bf-415">Un'app può dichiarare l'isolamento dei driver della stampante nel manifesto dell'applicazione per isolarsi dal driver della stampante e migliorarne l'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="102bf-415">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="102bf-416">Ovvero l'app non si arresterà in modo anomalo se il driver della stampante presenta un errore.</span><span class="sxs-lookup"><span data-stu-id="102bf-416">That is, the app won't crash if the printer driver has an error.</span></span>


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

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="102bf-417">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="102bf-417">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="102bf-418">Specifica se è abilitata la funzionalità di scorrimento a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="102bf-418">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="102bf-419">**True** indica che è abilitato.</span><span class="sxs-lookup"><span data-stu-id="102bf-419">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="102bf-420">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-420">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="102bf-421">msix</span><span class="sxs-lookup"><span data-stu-id="102bf-421">msix</span></span>

<span data-ttu-id="102bf-422">Specifica le informazioni di identità di un [pacchetto MSIX di tipo sparse](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) per l'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="102bf-422">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="102bf-423">Questo elemento è supportato in Windows 10, versione 2004 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="102bf-423">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="102bf-424">L'elemento **msix** deve trovarsi nello spazio dei nomi `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="102bf-424">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="102bf-425">Dispone degli attributi illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="102bf-425">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="102bf-426">Attributo</span><span class="sxs-lookup"><span data-stu-id="102bf-426">Attribute</span></span>   | <span data-ttu-id="102bf-427">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102bf-427">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102bf-428">**pubblicazione**</span><span class="sxs-lookup"><span data-stu-id="102bf-428">**publisher**</span></span>    | <span data-ttu-id="102bf-429">Descrive le informazioni del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-429">Describes the publisher information.</span></span> <span data-ttu-id="102bf-430">Questo valore deve corrispondere all'attributo **Publisher** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifesto del pacchetto sparse.</span><span class="sxs-lookup"><span data-stu-id="102bf-430">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="102bf-431">**packageName**</span><span class="sxs-lookup"><span data-stu-id="102bf-431">**packageName**</span></span> | <span data-ttu-id="102bf-432">Descrive il contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="102bf-432">Describes the contents of the package.</span></span> <span data-ttu-id="102bf-433">Questo valore deve corrispondere all'attributo **Name** nell'elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) del manifesto del pacchetto sparse.</span><span class="sxs-lookup"><span data-stu-id="102bf-433">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="102bf-434">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="102bf-434">**applicationId**</span></span>    | <span data-ttu-id="102bf-435">Identificatore univoco dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="102bf-435">The unique identifier of the application.</span></span> <span data-ttu-id="102bf-436">Questo valore deve corrispondere all'attributo **ID** nell'elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) nel manifesto del pacchetto sparse.</span><span class="sxs-lookup"><span data-stu-id="102bf-436">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

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

### <a name="heaptype"></a><span data-ttu-id="102bf-437">heapType</span><span class="sxs-lookup"><span data-stu-id="102bf-437">heapType</span></span>

<span data-ttu-id="102bf-438">Esegue l'override dell'implementazione dell'heap predefinita per le [API dell'heap Win32](../Memory/heap-functions.md) da usare.</span><span class="sxs-lookup"><span data-stu-id="102bf-438">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="102bf-439">Il valore **SegmentHeap** indica che verrà utilizzato l'heap del segmento.</span><span class="sxs-lookup"><span data-stu-id="102bf-439">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="102bf-440">Heap segmenti è un'implementazione moderna dell'heap che in genere riduce l'utilizzo complessivo della memoria.</span><span class="sxs-lookup"><span data-stu-id="102bf-440">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="102bf-441">Questo elemento è supportato in Windows 10, versione 2004 (Build 19041) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="102bf-441">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="102bf-442">Tutti gli altri valori vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="102bf-442">All other values are ignored.</span></span>

<span data-ttu-id="102bf-443">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="102bf-443">This element has no attributes.</span></span>

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

## <a name="example"></a><span data-ttu-id="102bf-444">Esempio</span><span class="sxs-lookup"><span data-stu-id="102bf-444">Example</span></span>

<span data-ttu-id="102bf-445">Di seguito è riportato un esempio di un manifesto dell'applicazione per un'applicazione denominata MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="102bf-445">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="102bf-446">L'applicazione utilizza l'assembly side-by-side di SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="102bf-446">The application consumes the SampleAssembly side-by-side assembly.</span></span>

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
