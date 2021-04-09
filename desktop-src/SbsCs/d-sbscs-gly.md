---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8912f24478f79be8aa00c963dc27cb46ec756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050142"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="01952-103">D (applicazioni isolate e assembly side-by-side)</span><span class="sxs-lookup"><span data-stu-id="01952-103">D (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="01952-104">[A](a-sbscs-gly.md) B C d E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="01952-104">[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="01952-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**AssemblyIdentity del contesto DEF**</span><span class="sxs-lookup"><span data-stu-id="01952-105"><span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF-context assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="01952-106">Sottoelemento **assemblyIdentity** che definisce l'assembly affiancato descritto dal manifesto.</span><span class="sxs-lookup"><span data-stu-id="01952-106">An **assemblyIdentity** subelement defining the side-by-side assembly described by the manifest.</span></span> <span data-ttu-id="01952-107">Un sottoelemento **assemblyIdentity** del contesto def è sempre il primo sottoelemento di un elemento **assembly** .</span><span class="sxs-lookup"><span data-stu-id="01952-107">A DEF-context **assemblyIdentity** subelement is always the first subelement of an **assembly** element.</span></span>

</dd> <dt>

<span data-ttu-id="01952-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**Conflitto di controllo delle versioni DLL**</span><span class="sxs-lookup"><span data-stu-id="01952-108"><span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**DLL versioning conflict**</span></span>
</dt> <dd>

<span data-ttu-id="01952-109">Problema di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="01952-109">Compatibility problem.</span></span> <span data-ttu-id="01952-110">Si verificano problemi di condivisione degli assembly quando un'applicazione installa una versione di un assembly condiviso che non è compatibile con la versione precedente installata.</span><span class="sxs-lookup"><span data-stu-id="01952-110">Assembly sharing problems occur when an application installs a version of a shared assembly that is not backward compatible with the previously installed version.</span></span> <span data-ttu-id="01952-111">Una soluzione per i conflitti di controllo delle versioni delle DLL consiste nell'utilizzare la condivisione di assembly affiancata e le applicazioni isolate.</span><span class="sxs-lookup"><span data-stu-id="01952-111">A solution to DLL versioning conflicts is to use side-by-side assembly sharing and isolated applications.</span></span> <span data-ttu-id="01952-112">Con la condivisione di assembly affiancati, è possibile eseguire contemporaneamente più versioni dello stesso assembly di Windows.</span><span class="sxs-lookup"><span data-stu-id="01952-112">With side-by-side assembly sharing, multiple versions of the same Windows assembly can run simultaneously.</span></span> <span data-ttu-id="01952-113">Gli sviluppatori possono scegliere l'assembly affiancato da usare.</span><span class="sxs-lookup"><span data-stu-id="01952-113">Developers can choose which side-by-side assembly to use.</span></span>

</dd> </dl>

 

 



