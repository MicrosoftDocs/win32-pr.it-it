---
description: Windows Installer è integrato con i criteri di restrizione software in Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Criteri di restrizione software e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314193"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="408c5-103">Criteri di restrizione software e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="408c5-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="408c5-104">Windows Installer è integrato con i criteri di restrizione software in Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="408c5-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="408c5-105">I criteri di restrizione software possono essere configurati tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="408c5-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="408c5-106">I criteri di restrizione software consentono a un amministratore di impedire agli amministratori e agli utenti non amministratori di eseguire file in base ai criteri percorso, zona URL, hash o editore.</span><span class="sxs-lookup"><span data-stu-id="408c5-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="408c5-107">I criteri di restrizione software hanno due livelli: senza restrizioni e non consentiti.</span><span class="sxs-lookup"><span data-stu-id="408c5-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="408c5-108">Il Windows Installer installa solo i pacchetti di cui è consentita l'esecuzione al livello Unrestricted.</span><span class="sxs-lookup"><span data-stu-id="408c5-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="408c5-109">È inoltre necessario consentire l'esecuzione di patch o trasformazioni a livello illimitato.</span><span class="sxs-lookup"><span data-stu-id="408c5-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="408c5-110">Se un pacchetto, una patch o una trasformazione è configurata per l'esecuzione a un livello diverso da Unrestricted, il Windows Installer Visualizza un messaggio di errore e registra una voce nel registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="408c5-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="408c5-111">I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene nuovamente memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="408c5-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="408c5-112">Se un pacchetto, una patch o una trasformazione è limitata, nel Windows Installer viene visualizzato un messaggio di errore e viene scritta una voce di [registrazione eventi](event-logging.md) nel registro eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="408c5-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="408c5-113">I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene nuovamente memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="408c5-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="408c5-114">Per ulteriori informazioni sui criteri di restrizione software, consultare la documentazione del prodotto e [cercare il sito TechNet](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="408c5-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



