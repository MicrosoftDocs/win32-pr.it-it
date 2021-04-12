---
description: Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione. Gli assembly privati devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231860"
---
# <a name="private-assemblies"></a><span data-ttu-id="96e5d-104">Assembly privati</span><span class="sxs-lookup"><span data-stu-id="96e5d-104">Private Assemblies</span></span>

<span data-ttu-id="96e5d-105">Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-105">A Win32 assembly can be installed as a private assembly and be exclusively available for use by one application.</span></span> <span data-ttu-id="96e5d-106">Gli assembly privati devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-106">Private assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="96e5d-107">In Windows XP gli assembly privati vengono installati come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="96e5d-107">On Windows XP, private assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="96e5d-108">Il Windows Installer installa gli assembly side-by-side privati in una cartella privata per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-108">The Windows Installer installs private side-by-side assemblies in a folder private to the application.</span></span> <span data-ttu-id="96e5d-109">Generalmente la cartella che contiene il file eseguibile delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="96e5d-109">Commonly the folder that contains the applications executable file.</span></span> <span data-ttu-id="96e5d-110">La dipendenza dell'applicazione nell'assembly privato viene specificata in un file manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-110">The dependency of the application on the private assembly is specified in an application manifest file.</span></span> <span data-ttu-id="96e5d-111">Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="96e5d-111">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="96e5d-112">Nei sistemi operativi precedenti a Windows XP, una copia dell'assembly privato e di un file con estensione local viene installata in una cartella privata per l'utilizzo esclusivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-112">On operating systems earlier than Windows XP, a copy of the private assembly and a .local file is installed into a private folder for the exclusive use of the application.</span></span> <span data-ttu-id="96e5d-113">Una versione dell'assembly viene anche registrata a livello globale nel sistema e disponibile per qualsiasi applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="96e5d-113">A version of the assembly is also globally registered on the system and available for any application that binds to it.</span></span> <span data-ttu-id="96e5d-114">La versione globale dell'assembly può essere la versione installata con l'applicazione o una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="96e5d-114">The global version of the assembly may be the version installed with the application or an earlier version.</span></span> <span data-ttu-id="96e5d-115">La versione globale è determinata dalle stesse regole utilizzate dai [componenti isolati](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="96e5d-115">The global version is determined by the same rules use by [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="96e5d-116">Si noti che il Windows Installer non è in grado di installare un assembly privato in una posizione con un percorso contenente più di 234 caratteri, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="96e5d-116">Note that the Windows Installer cannot install a private assembly in a location having a path that contains more than 234 characters, including the terminating null character.</span></span>

 

 
