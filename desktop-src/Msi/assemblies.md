---
description: Windows Installer possibile installare, rimuovere e aggiornare gli assembly e gli assembly Win32 utilizzati dall'Common Language Runtime di Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311052"
---
# <a name="assemblies"></a><span data-ttu-id="c6c58-103">Assembly</span><span class="sxs-lookup"><span data-stu-id="c6c58-103">Assemblies</span></span>

<span data-ttu-id="c6c58-104">Windows Installer possibile installare, rimuovere e aggiornare gli assembly e gli assembly Win32 utilizzati dall'Common Language Runtime di Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c6c58-104">Windows Installer can install, remove, and update Win32 assemblies and assemblies used by the common language runtime of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c6c58-105">Un assembly viene gestito dal Windows Installer come un singolo componente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c6c58-105">An assembly is handled by the Windows Installer as a single installer component.</span></span> <span data-ttu-id="c6c58-106">Tutti i file che costituiscono un assembly devono essere contenuti in un singolo componente del programma di installazione elencato nella tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c58-106">All of the files that constitute an assembly must be contained by a single installer component that is listed in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="c6c58-107">Windows Installer eseguiti in Windows Vista e Windows XP possono installare assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="c6c58-107">Windows Installer running on Windows Vista and Windows XP can install side-by-side assemblies.</span></span> <span data-ttu-id="c6c58-108">Gli assembly affiancati possono condividere in modo sicuro gli assembly tra più applicazioni e possono compensare gli effetti negativi della condivisione degli assembly, ad esempio i conflitti tra DLL.</span><span class="sxs-lookup"><span data-stu-id="c6c58-108">Side-by-side assemblies can safely share assemblies among multiple applications and can offset the negative effects of assembly sharing, such as DLL conflicts.</span></span> <span data-ttu-id="c6c58-109">Anziché una singola versione di un assembly che presuppone la compatibilità con le versioni precedenti di tutte le applicazioni, la condivisione di assembly affiancati consente l'esecuzione simultanea di più versioni di un assembly COM o Win32 nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6c58-109">Instead of a single version of an assembly that assumes backward compatibility with all applications, side-by-side assembly sharing enables multiple versions of a COM or Win32 assembly to run simultaneously on the system.</span></span> <span data-ttu-id="c6c58-110">Questa funzionalità migliorata per isolare le applicazioni è una parte importante del Framework Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="c6c58-110">This improved capability to isolate applications is an important part of the Microsoft .NET Framework.</span></span> <span data-ttu-id="c6c58-111">Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span><span class="sxs-lookup"><span data-stu-id="c6c58-111">For more information, see [Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).</span></span>

<span data-ttu-id="c6c58-112">Nelle sezioni seguenti viene descritto l'utilizzo degli assembly con il Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c6c58-112">The following sections describe the use of assemblies with the Windows Installer.</span></span>

-   [<span data-ttu-id="c6c58-113">Aggiunta di assembly a un pacchetto</span><span class="sxs-lookup"><span data-stu-id="c6c58-113">Adding Assemblies to a Package</span></span>](adding-assemblies-to-a-package.md)
-   [<span data-ttu-id="c6c58-114">Installazione e rimozione di assembly</span><span class="sxs-lookup"><span data-stu-id="c6c58-114">Installing and Removing Assemblies</span></span>](installing-and-removing-assemblies.md)
-   [<span data-ttu-id="c6c58-115">Aggiornamento degli assembly</span><span class="sxs-lookup"><span data-stu-id="c6c58-115">Updating Assemblies</span></span>](updating-assemblies.md)
-   [<span data-ttu-id="c6c58-116">Modalità di reinstallazione degli assembly Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="c6c58-116">Reinstallation Modes of Common Language Runtime Assemblies</span></span>](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [<span data-ttu-id="c6c58-117">Chiavi del registro di sistema dell'assembly scritte da Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c6c58-117">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)

<span data-ttu-id="c6c58-118">Per informazioni sull'installazione di applicazioni COM e COM+ 1,0, vedere [installazione di un'applicazione com+ con il Windows Installer](installing-a-com--application-with-the-windows-installer.md), [installazione di un componente com in un percorso privato](installing-a-com-component-to-a-private-location.md)e [rendere privato un componente com in un pacchetto esistente](make-a-com-component-in-an-existing-package-private.md).</span><span class="sxs-lookup"><span data-stu-id="c6c58-118">For information about installing COM and COM+ 1.0 applications, see [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installing a COM Component to a Private Location](installing-a-com-component-to-a-private-location.md), and [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).</span></span>

 

 
