---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311622"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="9175f-103">A (applicazioni isolate e assembly side-by-side)</span><span class="sxs-lookup"><span data-stu-id="9175f-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="9175f-104">A B C [d](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="9175f-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9175f-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contesto di attivazione**</span><span class="sxs-lookup"><span data-stu-id="9175f-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-106">Struttura di dati in memoria.</span><span class="sxs-lookup"><span data-stu-id="9175f-106">A data structure in memory.</span></span> <span data-ttu-id="9175f-107">Ogni sezione di questa struttura contiene i metadati per le funzioni API side-by-side.</span><span class="sxs-lookup"><span data-stu-id="9175f-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="9175f-108">Ad esempio, una sezione può avere dati di reindirizzamento DLL, che vengono usati dal caricatore della DLL e un altro potrebbe avere dati del server COM.</span><span class="sxs-lookup"><span data-stu-id="9175f-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="9175f-109">Questi dati possono essere utilizzati per reindirizzare il caricamento di una DLL a una versione specifica, la creazione di un oggetto COM o la creazione di una finestra a una versione più compatibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="9175f-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configurazione dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="9175f-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-111">Nomi e versioni degli assembly affiancati necessari per eseguire un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="9175f-112">Quando un'applicazione viene distribuita con un manifesto, le dipendenze da versioni specifiche degli assembly side-by-side condivise vengono definite in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="9175f-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="9175f-113">Per impostazione predefinita, la versione dell'assembly specificata nel manifesto è la versione usata al momento dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="9175f-114">Configurazione applicazione globale specifica la configurazione di tutte le applicazioni nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9175f-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="9175f-115">La configurazione per applicazione può eseguire l'override della configurazione dell'applicazione globale per ogni singola applicazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="9175f-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifesto di configurazione dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="9175f-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-117">File che specifica gli assembly affiancati che devono essere utilizzati da un'applicazione completamente o parzialmente isolata.</span><span class="sxs-lookup"><span data-stu-id="9175f-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="9175f-118">I file manifesto di configurazione dell'applicazione vengono installati nella stessa cartella del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="9175f-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifesto dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="9175f-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-120">File che descrive un'applicazione isolata.</span><span class="sxs-lookup"><span data-stu-id="9175f-120">File that describes an isolated application.</span></span> <span data-ttu-id="9175f-121">Specifica le informazioni necessarie per eseguire l'applicazione, incluse le dipendenze da assembly privati, versioni specifiche di assembly e metadati condivisi per gli assembly privati.</span><span class="sxs-lookup"><span data-stu-id="9175f-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="9175f-122">Il nome di un file manifesto dell'applicazione è il nome dell'eseguibile dell'applicazione seguito da Extension. manifest.</span><span class="sxs-lookup"><span data-stu-id="9175f-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="9175f-123">Ad esempio, per MySampleApp.exe, il file manifesto sarà MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="9175f-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="9175f-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span><span class="sxs-lookup"><span data-stu-id="9175f-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-125">Unità di base per la denominazione, l'associazione, il controllo delle versioni, la distribuzione o la configurazione di un blocco di codice di programmazione.</span><span class="sxs-lookup"><span data-stu-id="9175f-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="9175f-126">Questi assembly di codice possono essere inseriti in dll o assembly COM.</span><span class="sxs-lookup"><span data-stu-id="9175f-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="9175f-127">Le applicazioni con funzionalità comuni possono eseguire blocchi condivisi del codice di programmazione, detti moduli o assembly di codice.</span><span class="sxs-lookup"><span data-stu-id="9175f-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="9175f-128">L'infrastruttura per la condivisione sicura degli assembly è detta condivisione degli assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="9175f-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="9175f-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifesto dell'assembly**</span><span class="sxs-lookup"><span data-stu-id="9175f-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="9175f-130">Descrizione di un assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="9175f-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="9175f-131">Specifica il nome, la versione, i file, le risorse dell'assembly, i dati di associazione per gli elementi dell'assembly e le dipendenze da altri assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="9175f-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="9175f-132">Un file manifesto dell'assembly può avere qualsiasi nome file valido, purché sia seguito da Extension. manifest.</span><span class="sxs-lookup"><span data-stu-id="9175f-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



