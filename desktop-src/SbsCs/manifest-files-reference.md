---
description: Gli assembly affiancati vengono utilizzati con i tipi di file manifesto e di configurazione seguenti. I manifesti e le configurazioni sono file XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: "  File manifest"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128819"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="c96df-104">  File manifest</span><span class="sxs-lookup"><span data-stu-id="c96df-104">Manifest Files Reference</span></span>

<span data-ttu-id="c96df-105">Gli assembly affiancati vengono utilizzati con i tipi di file manifesto e di configurazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="c96df-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="c96df-106">I manifesti e le configurazioni sono file XML.</span><span class="sxs-lookup"><span data-stu-id="c96df-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="c96df-107">manifesto</span><span class="sxs-lookup"><span data-stu-id="c96df-107">Manifest</span></span>                                                               | <span data-ttu-id="c96df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c96df-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c96df-109">Manifesti dell'assembly</span><span class="sxs-lookup"><span data-stu-id="c96df-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="c96df-110">Descrive i nomi, le versioni, le risorse e le dipendenze degli assembly degli assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="c96df-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="c96df-111">Manifesti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c96df-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="c96df-112">Vengono descritti i nomi e le versioni degli assembly affiancati condivisi a cui l'applicazione deve essere associata in fase di esecuzione e possono inoltre contenere metadati per gli assembly side-by-side privati utilizzati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c96df-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="c96df-113">File di configurazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c96df-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="c96df-114">Reindirizza le versioni degli assembly delle dipendenze degli assembly usando la [configurazione per ogni applicazione](per-application-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="c96df-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="c96df-115">File di configurazione del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="c96df-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="c96df-116">Reindirizza le versioni degli assembly delle dipendenze degli assembly per ogni assembly utilizzando una configurazione del [server di pubblicazione](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="c96df-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="c96df-117">Per un elenco dello schema del file manifesto, vedere [schema del file manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c96df-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="c96df-118">Per un elenco dello schema del file di configurazione dell'applicazione, vedere [schema del file di configurazione dell'applicazione](application-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c96df-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="c96df-119">Per un elenco dello schema del file di configurazione dell'editore, vedere [schema del file di configurazione del server di pubblicazione](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c96df-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="c96df-120">Altre tecnologie estendono il formato utilizzato dai manifesti di configurazione e controllo delle versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="c96df-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="c96df-121">Gli sviluppatori devono fare riferimento alla documentazione specifica per la tecnologia usata per informazioni sul formato del manifesto.</span><span class="sxs-lookup"><span data-stu-id="c96df-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="c96df-122">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c96df-122">For example:</span></span>

-   [<span data-ttu-id="c96df-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="c96df-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="c96df-124">Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="c96df-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="c96df-125">[Controllo dell'account utente](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c96df-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
