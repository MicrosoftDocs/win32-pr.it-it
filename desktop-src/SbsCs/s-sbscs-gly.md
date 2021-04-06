---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: S (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9727db4c2db522b0bbb88eccf89481a61a75d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759041"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="779d9-103">S (applicazioni isolate e assembly side-by-side)</span><span class="sxs-lookup"><span data-stu-id="779d9-103">S (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="779d9-104">[A](a-sbscs-gly.md) B C [d](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="779d9-104">[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="779d9-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly affiancato condiviso**</span><span class="sxs-lookup"><span data-stu-id="779d9-105"><span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**shared side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="779d9-106">Un assembly affiancato condiviso è disponibile per l'utilizzo da parte di più applicazioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="779d9-106">A shared side-by-side assembly is available for use by multiple applications on the computer.</span></span> <span data-ttu-id="779d9-107">Viene installato nella cartella WinSxS della directory di Windows.</span><span class="sxs-lookup"><span data-stu-id="779d9-107">It is installed in the Winsxs folder of the Windows directory.</span></span> <span data-ttu-id="779d9-108">Le applicazioni e gli amministratori possono gestire la versione di un assembly condiviso da usare specificando la configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="779d9-108">Applications and administrators can manage the version of a shared assembly to be used by specifying the application configuration.</span></span> <span data-ttu-id="779d9-109">Gli assembly affiancati sono sempre accompagnati da file manifesto che forniscono informazioni sull'assembly al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="779d9-109">Side-by-side assemblies are always accompanied by manifest files that provide information about the assembly to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="779d9-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly affiancato**</span><span class="sxs-lookup"><span data-stu-id="779d9-110"><span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**side-by-side assembly**</span></span>
</dt> <dd>

<span data-ttu-id="779d9-111">Un assembly affiancato è un assembly Win32 accompagnato da manifesti.</span><span class="sxs-lookup"><span data-stu-id="779d9-111">A side-by-side assembly is a Win32 assembly accompanied by manifests.</span></span> <span data-ttu-id="779d9-112">Un assembly affiancato contiene una raccolta di risorse, ovvero un gruppo di dll, classi Windows, server COM, librerie dei tipi o interfacce, che vengono sempre fornite alle applicazioni insieme.</span><span class="sxs-lookup"><span data-stu-id="779d9-112">A side-by-side assembly contains a collection of resources—a group of DLLs, windows classes, COM servers, type libraries, or interfaces—that are always provided to applications together.</span></span>

</dd> <dt>

<span data-ttu-id="779d9-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**condivisione di assembly affiancati**</span><span class="sxs-lookup"><span data-stu-id="779d9-113"><span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**side-by-side assembly sharing**</span></span>
</dt> <dd>

<span data-ttu-id="779d9-114">Uso di assembly affiancati per condividere in modo sicuro gli assembly tra più applicazioni e per compensare gli effetti negativi della condivisione, ad esempio i conflitti tra DLL.</span><span class="sxs-lookup"><span data-stu-id="779d9-114">Use of side-by-side assemblies to safely share assemblies among multiple applications and to offset the negative effects of sharing, such as DLL conflicts.</span></span> <span data-ttu-id="779d9-115">Invece di avere una singola versione di un assembly che presuppone la compatibilità con le versioni precedenti di tutte le applicazioni, la condivisione di assembly affiancati consente l'esecuzione simultanea di più versioni di un assembly Win32 nel sistema.</span><span class="sxs-lookup"><span data-stu-id="779d9-115">Instead of having a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="779d9-116">Gli assembly affiancati sono sempre accompagnati da file manifesto dell'assembly che forniscono informazioni sull'assembly al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="779d9-116">Side-by-side assemblies are always accompanied by assembly manifest files that provide information about the assembly to the operating system.</span></span> <span data-ttu-id="779d9-117">Le applicazioni e gli amministratori possono gestire la condivisione degli assembly side-by-side dopo la distribuzione aggiornando la configurazione dell'applicazione in base a un'applicazione o globale.</span><span class="sxs-lookup"><span data-stu-id="779d9-117">Applications and administrators can manage side-by-side assembly sharing after deployment by updating the application configuration on either a global or per-application basis.</span></span>

</dd> </dl>

 

 



