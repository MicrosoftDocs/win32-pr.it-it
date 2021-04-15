---
description: È possibile installare assembly side-by-side come assembly condivisi o come assembly privati. Per ulteriori informazioni, vedere installazione di assembly side-by-side come assembly privati e installazione affiancata di assembly come assembly condivisi.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Installazione di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484637"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="601e3-104">Installazione di assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="601e3-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="601e3-105">È possibile installare assembly side-by-side come [assembly condivisi](/windows/desktop/Msi/shared-assemblies) o come [assembly privati](/windows/desktop/Msi/private-assemblies).</span><span class="sxs-lookup"><span data-stu-id="601e3-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="601e3-106">Per ulteriori informazioni, vedere [installazione di assembly side-by-side come assembly privati](installing-side-by-side-assemblies-as-private-assemblies.md) e [installazione affiancata di assembly come assembly condivisi](installing-side-by-side-assemblies-as-shared-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="601e3-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="601e3-107">Tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="601e3-107">Note that:</span></span>

-   <span data-ttu-id="601e3-108">Gli assembly installati nel Global Assembly Cache da un'installazione di che utilizza il [contesto di installazione](/windows/desktop/Msi/installation-context) per utente non sono protetti da protezione file di Windows.</span><span class="sxs-lookup"><span data-stu-id="601e3-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="601e3-109">Gli assembly installati nel Global Assembly Cache da un'installazione di tramite il [contesto di installazione](/windows/desktop/Msi/installation-context) per computer sono protetti da protezione file di Windows.</span><span class="sxs-lookup"><span data-stu-id="601e3-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
