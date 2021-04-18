---
description: Nella procedura seguente viene descritto come installare assembly side-by-side come assembly condivisi.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installazione di assembly side-by-side come assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484644"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a><span data-ttu-id="c6886-103">Installazione di assembly side-by-side come assembly condivisi</span><span class="sxs-lookup"><span data-stu-id="c6886-103">Installing Side-by-side Assemblies as Shared Assemblies</span></span>

<span data-ttu-id="c6886-104">Nella procedura seguente viene descritto come installare [assembly side-by-side](about-side-by-side-assemblies-.md) come [assembly condivisi](/windows/desktop/Msi/shared-assemblies).</span><span class="sxs-lookup"><span data-stu-id="c6886-104">The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](/windows/desktop/Msi/shared-assemblies).</span></span>

<span data-ttu-id="c6886-105">**Per installare un assembly side-by-side come assembly condiviso**</span><span class="sxs-lookup"><span data-stu-id="c6886-105">**To install a side-by-side assembly as a shared assembly**</span></span>

1.  <span data-ttu-id="c6886-106">Firmare e creare un catalogo per i file nell'assembly.</span><span class="sxs-lookup"><span data-stu-id="c6886-106">Sign and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="c6886-107">I file devono essere firmati per installarli come assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="c6886-107">Files must be signed to install them as side-by-side assemblies.</span></span> <span data-ttu-id="c6886-108">Per altre informazioni, vedere [creazione di file e cataloghi firmati](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="c6886-108">For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

2.  <span data-ttu-id="c6886-109">È necessario installare assembly side-by-side condivisi come componenti di un pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c6886-109">You should install shared side-by-side assemblies as components of a Windows Installer package.</span></span> <span data-ttu-id="c6886-110">Può trattarsi dello stesso pacchetto di installazione usato per installare o aggiornare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6886-110">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="c6886-111">Se l'assembly condiviso viene fornito come parte di più applicazioni, è necessario fornire un modulo merge che può essere incorporato nei pacchetti di installazione di tali applicazioni e creare un catalogo per i file nell'assembly.</span><span class="sxs-lookup"><span data-stu-id="c6886-111">If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.</span></span>

    <span data-ttu-id="c6886-112">Per installare gli assembly è necessario Windows Installer versione 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c6886-112">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="c6886-113">Per ulteriori informazioni, vedere il [Windows Installer](../msi/windows-installer-portal.md) SDK e le sezioni in [installazione degli assembly Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="c6886-113">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

 

 
