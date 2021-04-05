---
description: Un file di configurazione del server di pubblicazione è un file XML che reindirizza a livello globale le applicazioni e gli assembly usando una versione di un assembly affiancato a un'altra versione dello stesso assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: File di configurazione del server di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884533"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="571fb-103">File di configurazione del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="571fb-103">Publisher Configuration Files</span></span>

<span data-ttu-id="571fb-104">Un file di configurazione del server di pubblicazione è un file XML che reindirizza a livello globale le applicazioni e gli assembly usando una versione di un assembly affiancato a un'altra versione dello stesso assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="571fb-105">In genere, l'autore dell'assembly rilascia un aggiornamento compatibile o una correzione della sicurezza per ogni assembly mediante l'emissione di un file di configurazione dell'editore da installare insieme a un Service Pack aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="571fb-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="571fb-106">Questa operazione viene definita [configurazione del server di pubblicazione](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="571fb-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="571fb-107">Per ulteriori informazioni su questo tipo di [configurazione](configuration.md) , vedere Configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="571fb-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="571fb-108">I file di configurazione del server di pubblicazione presentano gli elementi e gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="571fb-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="571fb-109">Per un elenco completo dei XML Schema, vedere [schema del file di configurazione dell'editore](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="571fb-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="571fb-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="571fb-110">Element</span></span>               | <span data-ttu-id="571fb-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="571fb-111">Attributes</span></span>                | <span data-ttu-id="571fb-112">Necessario</span><span class="sxs-lookup"><span data-stu-id="571fb-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="571fb-113">**assembly**</span><span class="sxs-lookup"><span data-stu-id="571fb-113">**assembly**</span></span>          |                           | <span data-ttu-id="571fb-114">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-114">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-115">**manifestVersion**</span></span>       | <span data-ttu-id="571fb-116">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-116">Yes</span></span>      |
| <span data-ttu-id="571fb-117">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="571fb-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="571fb-118">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-118">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-119">**type**</span><span class="sxs-lookup"><span data-stu-id="571fb-119">**type**</span></span>                  | <span data-ttu-id="571fb-120">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-120">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-121">**nome**</span><span class="sxs-lookup"><span data-stu-id="571fb-121">**name**</span></span>                  | <span data-ttu-id="571fb-122">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-122">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-123">**language**</span><span class="sxs-lookup"><span data-stu-id="571fb-123">**language**</span></span>              | <span data-ttu-id="571fb-124">No</span><span class="sxs-lookup"><span data-stu-id="571fb-124">No</span></span>       |
|                       | <span data-ttu-id="571fb-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="571fb-125">**processorArchitecture**</span></span> | <span data-ttu-id="571fb-126">No</span><span class="sxs-lookup"><span data-stu-id="571fb-126">No</span></span>       |
|                       | <span data-ttu-id="571fb-127">**version**</span><span class="sxs-lookup"><span data-stu-id="571fb-127">**version**</span></span>               | <span data-ttu-id="571fb-128">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-128">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="571fb-129">**publicKeyToken**</span></span>        | <span data-ttu-id="571fb-130">No</span><span class="sxs-lookup"><span data-stu-id="571fb-130">No</span></span>       |
| <span data-ttu-id="571fb-131">**dipendenza**</span><span class="sxs-lookup"><span data-stu-id="571fb-131">**dependency**</span></span>        |                           | <span data-ttu-id="571fb-132">No</span><span class="sxs-lookup"><span data-stu-id="571fb-132">No</span></span>       |
| <span data-ttu-id="571fb-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="571fb-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="571fb-134">No</span><span class="sxs-lookup"><span data-stu-id="571fb-134">No</span></span>       |
| <span data-ttu-id="571fb-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="571fb-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="571fb-136">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-136">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-137">**oldVersion**</span></span>            | <span data-ttu-id="571fb-138">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-138">Yes</span></span>      |
|                       | <span data-ttu-id="571fb-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-139">**newVersion**</span></span>            | <span data-ttu-id="571fb-140">Sì</span><span class="sxs-lookup"><span data-stu-id="571fb-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="571fb-141">Percorso file</span><span class="sxs-lookup"><span data-stu-id="571fb-141">File Location</span></span>

<span data-ttu-id="571fb-142">I file di configurazione del server di pubblicazione devono essere installati nella cartella WinSxS.</span><span class="sxs-lookup"><span data-stu-id="571fb-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="571fb-143">Vengono in genere installate come file separati, ma i file di configurazione del server di pubblicazione possono essere inclusi anche come risorsa in una DLL.</span><span class="sxs-lookup"><span data-stu-id="571fb-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="571fb-144">Un file di configurazione del server di pubblicazione non può essere incluso come risorsa in un file EXE.</span><span class="sxs-lookup"><span data-stu-id="571fb-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="571fb-145">Un file EXE può includere un [manifesto dell'applicazione](application-manifests.md) come risorsa.</span><span class="sxs-lookup"><span data-stu-id="571fb-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="571fb-146">Sintassi del nome file</span><span class="sxs-lookup"><span data-stu-id="571fb-146">File Name Syntax</span></span>

<span data-ttu-id="571fb-147">Il nome file di un file di configurazione del server di pubblicazione ha il formato *criterio*. *principale*. *minore*. *AssemblyName* dove *Major* e *minor* fanno riferimento alle parti principali e secondarie della [versione dell'assembly](assembly-versions.md) interessata.</span><span class="sxs-lookup"><span data-stu-id="571fb-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="571fb-148">*AssemblyName* fa riferimento al nome dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="571fb-149">Ad esempio, un file di configurazione del server di pubblicazione per la versione 6,0 dell'assembly Microsoft. Windows. Common-Controls avrà il nome seguente:</span><span class="sxs-lookup"><span data-stu-id="571fb-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="571fb-150">Policy. 6.0. Microsoft. Windows. Common-Controls</span><span class="sxs-lookup"><span data-stu-id="571fb-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="571fb-151">Non usare i file di configurazione dei criteri per incrementare la versione principale o secondaria di un assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="571fb-152">Ad esempio, non reindirizzare la versione 6.0.0.0 a 7.0.0.0 o versione 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="571fb-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="571fb-153">Quando un'applicazione fa riferimento a una versione dell'assembly, ad esempio 6.0.0.0, viene verificata la presenza di eventuali file di configurazione dei criteri con le versioni principale e secondaria specificate, ad esempio 6,0.</span><span class="sxs-lookup"><span data-stu-id="571fb-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="571fb-154">L'applicazione viene quindi reindirizzata a un'altra versione dell'assembly, ad esempio 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="571fb-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="571fb-155">Se un file di configurazione del server di pubblicazione incrementa la versione principale o secondaria di un assembly, il reindirizzamento successivo dell'assembly potrebbe richiedere l'emissione di più file di configurazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="571fb-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="571fb-156">Elementi</span><span class="sxs-lookup"><span data-stu-id="571fb-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="571fb-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span><span class="sxs-lookup"><span data-stu-id="571fb-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="571fb-158">Elemento contenitore.</span><span class="sxs-lookup"><span data-stu-id="571fb-158">A container element.</span></span> <span data-ttu-id="571fb-159">Il primo sottoelemento deve essere un elemento **assemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="571fb-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="571fb-160">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="571fb-160">Required.</span></span>

<span data-ttu-id="571fb-161">L'elemento assembly deve trovarsi nello spazio dei nomi **urn: schemas-microsoft-com: ASM. V1**.</span><span class="sxs-lookup"><span data-stu-id="571fb-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="571fb-162">Gli elementi figlio dell'assembly devono trovarsi anche in questo spazio dei nomi, in base all'ereditarietà o all'assegnazione di tag.</span><span class="sxs-lookup"><span data-stu-id="571fb-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="571fb-163">L'elemento **assembly** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="571fb-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="571fb-164">Attributo</span><span class="sxs-lookup"><span data-stu-id="571fb-164">Attribute</span></span>           | <span data-ttu-id="571fb-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571fb-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="571fb-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-166">**manifestVersion**</span></span> | <span data-ttu-id="571fb-167">L'attributo **manifestVersion** deve essere impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="571fb-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="571fb-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="571fb-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="571fb-169">Descrive e identifica in modo univoco un assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="571fb-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="571fb-170">Come primo sottoelemento di un elemento **assembly** , **assemblyIdentity** descrive l'assembly affiancato in cui sono state modificate una o più delle relative dipendenze di assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="571fb-171">Il file di configurazione del server di pubblicazione reindirizza le dipendenze dell'assembly identificato.</span><span class="sxs-lookup"><span data-stu-id="571fb-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="571fb-172">Il seguente **assemblyIdentity** indica, ad esempio, che il file di configurazione del server di pubblicazione influisca sulle dipendenze dell'assembly Microsoft. Windows. pop 6.0.0.0 x86.</span><span class="sxs-lookup"><span data-stu-id="571fb-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="571fb-173">Come primo sottoelemento di un elemento **dependentAssembly** , **assemblyIdentity** descrive una dipendenza di assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="571fb-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="571fb-174">Il file di configurazione del server di pubblicazione riconfigura l'identità dell'assembly side-by-side richiesto.</span><span class="sxs-lookup"><span data-stu-id="571fb-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="571fb-175">La modifica viene specificata in un **bindingRedirect**.</span><span class="sxs-lookup"><span data-stu-id="571fb-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="571fb-176">Ad esempio, il codice **assemblyIdentity** seguente modifica qualsiasi dipendenza da Microsoft. Windows. SampleAssembly versione 2.0.0.0 a una dipendenza da Microsoft. Windows. SampleAssembly versione 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="571fb-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="571fb-177">L'elemento **assemblyIdentity** ha gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="571fb-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="571fb-178">Non contiene sottoelementi.</span><span class="sxs-lookup"><span data-stu-id="571fb-178">It has no sub-elements.</span></span>



| <span data-ttu-id="571fb-179">Attributo</span><span class="sxs-lookup"><span data-stu-id="571fb-179">Attribute</span></span>                 | <span data-ttu-id="571fb-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571fb-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="571fb-181">**type**</span><span class="sxs-lookup"><span data-stu-id="571fb-181">**type**</span></span>                  | <span data-ttu-id="571fb-182">Specifica il tipo di assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-182">Specifies the assembly type.</span></span> <span data-ttu-id="571fb-183">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="571fb-183">Required.</span></span> <span data-ttu-id="571fb-184">In **assemblyIdentity** per l'assembly interessato, il valore dell'attributo **Type** deve essere impostato su Win32-Policy.</span><span class="sxs-lookup"><span data-stu-id="571fb-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="571fb-185">Il valore Win32-Policy deve essere in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="571fb-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="571fb-186">In **assemblyIdentity** per la dipendenza di assembly modificabile, il valore dell'attributo **Type** deve essere impostato su Win32.</span><span class="sxs-lookup"><span data-stu-id="571fb-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="571fb-187">Il valore Win32 deve essere in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="571fb-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="571fb-188">**nome**</span><span class="sxs-lookup"><span data-stu-id="571fb-188">**name**</span></span>                  | <span data-ttu-id="571fb-189">Assegna un nome univoco a un assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-189">Uniquely names an assembly.</span></span> <span data-ttu-id="571fb-190">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="571fb-190">Required.</span></span> <span data-ttu-id="571fb-191">In **assemblyIdentity** per l'assembly interessato, il nome ha i *criteri* del modulo. *principale*. *minore*. *AssemblyName* dove *Major* e *minor* fanno riferimento alle parti principali e secondarie della [versione dell'assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="571fb-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="571fb-192">In **assemblyIdentity** per la dipendenza di assembly in modifica, il nome ha il formato Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="571fb-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="571fb-193">Ad esempio, Microsoft. Windows. MysampleApp.</span><span class="sxs-lookup"><span data-stu-id="571fb-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="571fb-194">**language**</span><span class="sxs-lookup"><span data-stu-id="571fb-194">**language**</span></span>              | <span data-ttu-id="571fb-195">Identifica la lingua dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="571fb-196">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="571fb-196">Optional.</span></span> <span data-ttu-id="571fb-197">In **assemblyIdentity** per l'assembly interessato, se l'assembly è specifico della lingua, specificare il codice della lingua DHTML.</span><span class="sxs-lookup"><span data-stu-id="571fb-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="571fb-198">Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), omettere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="571fb-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="571fb-199">In **assemblyIdentity** per la dipendenza di assembly modificabile, se l'assembly è specifico della lingua, specificare il codice della lingua DHTML.</span><span class="sxs-lookup"><span data-stu-id="571fb-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="571fb-200">Se l'assembly è per l'uso in tutto il mondo (indipendente dalla lingua), impostare il valore come " \* ".</span><span class="sxs-lookup"><span data-stu-id="571fb-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="571fb-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="571fb-201">**processorArchitecture**</span></span> | <span data-ttu-id="571fb-202">Specifica il processore che esegue l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="571fb-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="571fb-203">**version**</span><span class="sxs-lookup"><span data-stu-id="571fb-203">**version**</span></span>               | <span data-ttu-id="571fb-204">Specifica la versione dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-204">Specifies the assembly version.</span></span> <span data-ttu-id="571fb-205">Usare la sintassi di versione in quattro parti: mmmm. nnnn. oooo. pppp</span><span class="sxs-lookup"><span data-stu-id="571fb-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="571fb-206">Obbligatorio solo nel contesto di definizione **assemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="571fb-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="571fb-207">Non specificare l'attributo Version nell'oggetto **assemblyIdentity** del contesto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="571fb-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="571fb-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="571fb-208">**publicKeyToken**</span></span>        | <span data-ttu-id="571fb-209">Stringa esadecimale di 16 caratteri che rappresenta gli ultimi 8 byte dell'hash SHA-1 della chiave pubblica in cui è firmato l'assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="571fb-210">La chiave pubblica usata per firmare il catalogo deve essere di 2048 bit o superiore.</span><span class="sxs-lookup"><span data-stu-id="571fb-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="571fb-211">Un publicKeyToken è obbligatorio per tutti gli assembly affiancati condivisi.</span><span class="sxs-lookup"><span data-stu-id="571fb-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="571fb-212">Il publicKeyToken utilizzato per il file di configurazione del server di pubblicazione deve essere la stessa chiave utilizzata per l'assembly firmato.</span><span class="sxs-lookup"><span data-stu-id="571fb-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="571fb-213">I file di configurazione del server di pubblicazione possono essere firmati usando gli stessi strumenti usati con gli assembly, vedere [esempio di firma di assembly](assembly-signing-example.md) e creazione di [file e cataloghi firmati](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="571fb-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="571fb-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dipendenza**</span><span class="sxs-lookup"><span data-stu-id="571fb-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="571fb-215">Elemento contenitore facoltativo per almeno un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="571fb-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="571fb-216">Non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="571fb-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="571fb-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="571fb-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="571fb-218">Ogni **dependentAssembly** deve trovarsi all'interno di una sola **dipendenza**.</span><span class="sxs-lookup"><span data-stu-id="571fb-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="571fb-219">Un **dependentAssembly** non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="571fb-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="571fb-220">Il primo sottoelemento di **dependentAssembly** deve essere un **assemblyIdentity** per l'assembly affiancato riconfigurato dalla configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="571fb-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="571fb-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="571fb-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="571fb-222">L'elemento **bindingRedirect** contiene informazioni di reindirizzamento per l'associazione dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="571fb-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="571fb-223">Questo elemento ha gli attributi mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="571fb-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="571fb-224">Attributo</span><span class="sxs-lookup"><span data-stu-id="571fb-224">Attribute</span></span>      | <span data-ttu-id="571fb-225">Descrizione</span><span class="sxs-lookup"><span data-stu-id="571fb-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="571fb-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-226">**oldVersion**</span></span> | <span data-ttu-id="571fb-227">Specifica la versione dell'assembly sottoposta a override e reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="571fb-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="571fb-228">Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN.</span><span class="sxs-lookup"><span data-stu-id="571fb-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="571fb-229">Specificare un intervallo di versioni di un trattino senza spazi.</span><span class="sxs-lookup"><span data-stu-id="571fb-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="571fb-230">Ad esempio, 2.14.3.0 o 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="571fb-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="571fb-231">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="571fb-231">Required.</span></span> |
| <span data-ttu-id="571fb-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="571fb-232">**newVersion**</span></span> | <span data-ttu-id="571fb-233">Specifica la versione dell'assembly sostitutivo.</span><span class="sxs-lookup"><span data-stu-id="571fb-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="571fb-234">Usare la sintassi di versione in quattro parti nnnnn. NNNNN. NNNNN. NNNNN.</span><span class="sxs-lookup"><span data-stu-id="571fb-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="571fb-235">Commenti</span><span class="sxs-lookup"><span data-stu-id="571fb-235">Remarks</span></span>

<span data-ttu-id="571fb-236">I file di configurazione del server di pubblicazione non specificano i file.</span><span class="sxs-lookup"><span data-stu-id="571fb-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="571fb-237">Si noti che i file di criteri specifici della lingua sono separati dal file di configurazione del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="571fb-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="571fb-238">Esempio</span><span class="sxs-lookup"><span data-stu-id="571fb-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




