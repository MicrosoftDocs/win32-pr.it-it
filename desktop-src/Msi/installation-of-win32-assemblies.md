---
description: Installare gli assembly Win32 rendendoli un componente di Microsoft Windows Installer pacchetto che installa o aggiorna l'applicazione.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installazione degli assembly Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308898"
---
# <a name="installation-of-win32-assemblies"></a><span data-ttu-id="38c5a-103">Installazione degli assembly Win32</span><span class="sxs-lookup"><span data-stu-id="38c5a-103">Installation of Win32 Assemblies</span></span>

<span data-ttu-id="38c5a-104">Installare gli assembly Win32 rendendoli un componente di Microsoft Windows Installer pacchetto che installa o aggiorna l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38c5a-104">Install Win32 assemblies by making them a component of Microsoft Windows Installer package that installs or updates your application.</span></span> <span data-ttu-id="38c5a-105">Quando si creano la tabella [MsiAssembly](msiassembly-table.md) e la [tabella MsiAssemblyName](msiassemblyname-table.md), il componente viene identificato \_ come assembly nella colonna Component.</span><span class="sxs-lookup"><span data-stu-id="38c5a-105">When you author the [MsiAssembly table](msiassembly-table.md) and [MsiAssemblyName table](msiassemblyname-table.md), this identifies the component in the Component\_ column as an assembly.</span></span> <span data-ttu-id="38c5a-106">Il programma di installazione imposterà la proprietà [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) sulla versione del file di Sxs.dll nei sistemi operativi che possono supportare gli assembly Win32 senza impostare questa proprietà in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="38c5a-106">The installer will set the [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) property to the file version of Sxs.dll on operating systems that can support Win32 assemblies and not set this property otherwise.</span></span>

<span data-ttu-id="38c5a-107">In Windows Vista e Windows XP, Windows Installer non scrive informazioni sull'assembly nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="38c5a-107">In Windows Vista and Windows XP, Windows Installer does not write assembly information into the registry.</span></span> <span data-ttu-id="38c5a-108">È inoltre possibile utilizzare assembly condivisi, assembly privati e assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="38c5a-108">In addition, shared assemblies, private assemblies, and side-by-side assemblies can be used.</span></span> <span data-ttu-id="38c5a-109">Per informazioni, vedere assembly [condivisi](shared-assemblies.md), [assembly privati](private-assemblies.md)e [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="38c5a-109">For information, see [Shared Assemblies](shared-assemblies.md), [Private Assemblies](private-assemblies.md), and [Side-by-Side Assemblies](side-by-side-assemblies.md).</span></span>

<span data-ttu-id="38c5a-110">Nelle sezioni seguenti viene descritto come creare un pacchetto di Windows Installer per installare assembly Win32 come condiviso, privato o affiancato in diversi sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="38c5a-110">The following sections describe how to author a Windows Installer package to install Win32 assemblies as shared, private, or side-by-side on different Windows operating systems.</span></span>

-   [<span data-ttu-id="38c5a-111">Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP</span><span class="sxs-lookup"><span data-stu-id="38c5a-111">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="38c5a-112">Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP</span><span class="sxs-lookup"><span data-stu-id="38c5a-112">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



