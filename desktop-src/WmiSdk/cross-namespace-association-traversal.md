---
description: A partire da Windows 7, Strumentazione gestione Windows (WMI) ha implementato un meccanismo standard per individuare i profili mediante lo schema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Attraversamento dell'associazione tra spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880673"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="d855d-103">Attraversamento dell'associazione tra spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="d855d-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="d855d-104">A partire da Windows 7, Strumentazione gestione Windows (WMI) ha implementato un meccanismo standard per individuare i profili mediante lo schema CIM.</span><span class="sxs-lookup"><span data-stu-id="d855d-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="d855d-105">WMI supporta l'attraversamento dell'associazione tra spazi dei nomi e la registrazione del profilo di associazione.</span><span class="sxs-lookup"><span data-stu-id="d855d-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="d855d-106">Per ulteriori informazioni sulla registrazione del profilo e sull'implementazione standard CIM dell'attraversamento delle associazioni, vedere DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) ).</span><span class="sxs-lookup"><span data-stu-id="d855d-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="d855d-107">Per supportare questa funzionalità, l'infrastruttura WMI ha fatto quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d855d-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="d855d-108">Creazione dello spazio dei nomi Interop: \\ \\ interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="d855d-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="d855d-109">Attraversamento dell'associazione tra spazi dei nomi consentiti.</span><span class="sxs-lookup"><span data-stu-id="d855d-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="d855d-110">Le associazioni che incrociano gli spazi dei nomi supportano il filtro a livello di classe di associazione e a livello di spazio dei nomi implementato.</span><span class="sxs-lookup"><span data-stu-id="d855d-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="d855d-111">Sono state aggiunte le classi CIM [**\_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)e [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="d855d-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="d855d-112">Compatibilità 2.17.1 della versione dello schema CIM implementata.</span><span class="sxs-lookup"><span data-stu-id="d855d-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="d855d-113">Per ulteriori informazioni, vedere [CIM schema Compatibility](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="d855d-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="d855d-114">Spazio dei nomi Interop</span><span class="sxs-lookup"><span data-stu-id="d855d-114">Interop Namespace</span></span>

<span data-ttu-id="d855d-115">Lo spazio dei nomi Interop fornisce un percorso comune per l'individuazione da parte di un'applicazione client di tutti i profili supportati in un computer.</span><span class="sxs-lookup"><span data-stu-id="d855d-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="d855d-116">I profili possono essere usati per gestire vari aspetti di un sistema operativo, di un array di archiviazione o di un database.</span><span class="sxs-lookup"><span data-stu-id="d855d-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="d855d-117">Tutti gli oggetti e le classi di interoperabilità devono essere definiti nello \\ spazio dei nomi interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="d855d-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="d855d-118">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="d855d-118">CIM Classes</span></span>

<span data-ttu-id="d855d-119">Le classi CIM descritte nell'elenco seguente supportano l'attraversamento dell'associazione tra spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d855d-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="d855d-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d855d-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="d855d-121">Utilizzato per identificare la specifica del profilo che viene annunciata come implementata.</span><span class="sxs-lookup"><span data-stu-id="d855d-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="d855d-122">Questa classe specifica le informazioni che includono il nome del profilo, l'organizzazione e la versione con cui è conforme l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="d855d-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="d855d-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="d855d-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="d855d-124">Utilizzato per associare istanze di elementi di gestione definiti nei profili con la classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) che identifica le specifiche specifiche del profilo implementate.</span><span class="sxs-lookup"><span data-stu-id="d855d-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="d855d-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="d855d-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="d855d-126">Utilizzato per rappresentare la relazione tra profili.</span><span class="sxs-lookup"><span data-stu-id="d855d-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="d855d-127">Implementazione dell'attraversamento di associazioni tra spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="d855d-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="d855d-128">Il servizio WMI consente l'attraversamento dell'associazione tra spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d855d-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="d855d-129">WMI fornisce lo spazio dei nomi di interoperabilità per registrare i profili e associarli a profili implementati in spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="d855d-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="d855d-130">Tuttavia, per usare l'attraversamento dell'associazione, gli implementatori devono creare un'istanza delle classi di profilo sia nell'interoperabilità che nello spazio dei nomi implementato.</span><span class="sxs-lookup"><span data-stu-id="d855d-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="d855d-131">Per ulteriori informazioni, vedere [scrittura di un provider di associazioni per l'interoperabilità](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="d855d-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="d855d-132">Le associazioni che incrociano gli spazi dei nomi all'interno dello stesso ambiente di gestione devono essere create in entrambi gli spazi dei nomi di interoperabilità e implementato.</span><span class="sxs-lookup"><span data-stu-id="d855d-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="d855d-133">In caso contrario, l'attraversamento dell'associazione non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="d855d-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="d855d-134">Ad esempio, il provider di associazioni Power profile deve essere registrato con gli spazi dei nomi root/Interop e root/cimv2/Power.</span><span class="sxs-lookup"><span data-stu-id="d855d-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="d855d-135">L'attraversamento dell'associazione dovrebbe essere in grado di essere eseguito da uno spazio dei nomi all'altro.</span><span class="sxs-lookup"><span data-stu-id="d855d-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="d855d-136">Per esempi di attraversamento delle associazioni, vedere [accesso ai dati nello spazio dei nomi Interop](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="d855d-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="d855d-137">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="d855d-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="d855d-138">Dopo l'aggiornamento a Windows 7, se sono presenti profili di dispositivo di interoperabilità precedentemente installati nello spazio dei nomi radice/interoperabilità, non verrà installato alcun profilo di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d855d-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="d855d-139">Questi oggetti profilo di terze parti sovrascrivono lo schema di interoperabilità di Windows 7 per mantenere la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d855d-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="d855d-140">Inoltre, viene registrato l'evento dell'applicazione WMI con ID 5631.</span><span class="sxs-lookup"><span data-stu-id="d855d-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="d855d-141">Per ottenere i profili di interoperabilità di Windows 7, è necessario compilare la versione di Windows 7 del file Interop. mof e i file MFL correlati.</span><span class="sxs-lookup"><span data-stu-id="d855d-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="d855d-142">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="d855d-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d855d-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d855d-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d855d-144">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d855d-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d855d-145">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="d855d-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="d855d-146">**\_REFERENCEDPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="d855d-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="d855d-147">Compatibilità con lo schema CIM</span><span class="sxs-lookup"><span data-stu-id="d855d-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="d855d-148">Scrittura di un provider di associazioni per l'interoperabilità</span><span class="sxs-lookup"><span data-stu-id="d855d-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="d855d-149">Accesso ai dati nello spazio dei nomi Interop</span><span class="sxs-lookup"><span data-stu-id="d855d-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
