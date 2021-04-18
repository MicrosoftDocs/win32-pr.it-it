---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 904FE2AB-9E94-47E4-88BA-DB215775797B
title: G (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a4488c03da1c4c1f568db039a8b0e0a05d60ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306479"
---
# <a name="g-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="f80b5-103">G (applicazioni isolate e assembly side-by-side)</span><span class="sxs-lookup"><span data-stu-id="f80b5-103">G (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="f80b5-104">[A](a-sbscs-gly.md) B C [d](d-sbscs-gly.md) E F G H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="f80b5-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F G H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f80b5-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**configurazione dell'applicazione globale**</span><span class="sxs-lookup"><span data-stu-id="f80b5-105"><span id="_win32_global_application_configuration_gly"></span><span id="_WIN32_GLOBAL_APPLICATION_CONFIGURATION_GLY"></span>**global application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="f80b5-106">Specifica che tutte le applicazioni nel sistema utilizzano la stessa versione di assembly affiancata.</span><span class="sxs-lookup"><span data-stu-id="f80b5-106">Specification that all applications on the system use the same side-by-side assembly version.</span></span> <span data-ttu-id="f80b5-107">La configurazione globale viene specificata per singolo assembly in un file manifesto dell'assembly globale installato nella cartella WinSxS.</span><span class="sxs-lookup"><span data-stu-id="f80b5-107">Global configuration is specified on a per-assembly basis in a global assembly manifest file installed in the Winsxs folder.</span></span> <span data-ttu-id="f80b5-108">La configurazione globale potrebbe essere utilizzata quando uno sviluppatore o un amministratore di assembly deve configurare tutte le applicazioni nel sistema per l'utilizzo di una versione più recente dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="f80b5-108">Global configuration might be used when an assembly developer or administrator needs to configure all applications on the system to use a newer assembly version.</span></span> <span data-ttu-id="f80b5-109">In questo caso, il nuovo assembly deve essere compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="f80b5-109">In this case, the new assembly needs to be backward compatible.</span></span> <span data-ttu-id="f80b5-110">Una configurazione per applicazione esegue l'override della configurazione dell'applicazione predefinita o globale per applicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="f80b5-110">A per-application configuration overrides the default or global application configuration for specific applications.</span></span>

</dd> <dt>

<span data-ttu-id="f80b5-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**manifesto assembly globale**</span><span class="sxs-lookup"><span data-stu-id="f80b5-111"><span id="_win32_global_assembly_manifest_gly"></span><span id="_WIN32_GLOBAL_ASSEMBLY_MANIFEST_GLY"></span>**global assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="f80b5-112">File che definisce la configurazione dell'applicazione globale di un assembly affiancato.</span><span class="sxs-lookup"><span data-stu-id="f80b5-112">File that defines the global application configuration of a side-by-side assembly.</span></span> <span data-ttu-id="f80b5-113">I file manifesto dell'assembly globale vengono installati nell'archivio di assembly di sistema nella cartella WinSxS.</span><span class="sxs-lookup"><span data-stu-id="f80b5-113">Global assembly manifest files are installed into the system assembly store in the Winsxs folder.</span></span>

</dd> </dl>

 

 



