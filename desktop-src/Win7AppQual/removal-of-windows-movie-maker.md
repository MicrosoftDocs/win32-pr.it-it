---
description: .
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Rimozione di Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a3336421ae2bde761aa1d4f238b5cd135ba64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317616"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="0b2bd-103">Rimozione di Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="0b2bd-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0b2bd-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="0b2bd-104">Affected Platforms</span></span>

<span data-ttu-id="0b2bd-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b2bd-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="0b2bd-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b2bd-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="0b2bd-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="0b2bd-107">Feature Impact</span></span>

 <span data-ttu-id="0b2bd-108">**Gravità** -alta</span><span class="sxs-lookup"><span data-stu-id="0b2bd-108">**Severity** - High</span></span>  
<span data-ttu-id="0b2bd-109">**Frequenza** -media</span><span class="sxs-lookup"><span data-stu-id="0b2bd-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="0b2bd-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b2bd-110">Description</span></span>

<span data-ttu-id="0b2bd-111">Microsoft sta deprecando e rimuovendo l'utilità Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="0b2bd-112">ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0b2bd-112">This includes:</span></span>

-   <span data-ttu-id="0b2bd-113">Tutti i punti di ingresso di Windows Movie Maker (ad esempio, menu Start, avvio > esecuzione)</span><span class="sxs-lookup"><span data-stu-id="0b2bd-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="0b2bd-114">Tutti i file binari usati da Windows Movie Maker (tutti gli elementi presenti in% ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="0b2bd-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="0b2bd-115">Tuttavia, i file di progetto di un utente Movie Maker rimarranno nel sistema e saranno accessibili ad altre applicazioni che supportano questo formato di file.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0b2bd-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="0b2bd-116">Manifestation</span></span>

<span data-ttu-id="0b2bd-117">La rimozione di Windows Movie Maker comporta le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="0b2bd-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="0b2bd-118">Qualsiasi tentativo di avviare Windows Movie Maker con i relativi argomenti della riga di comando avrà esito negativo</span><span class="sxs-lookup"><span data-stu-id="0b2bd-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="0b2bd-119">Tutti i plug-in installati per abilitare nuove trasformazioni e animazioni rimarranno installati ma non verranno esposti all'utente finale</span><span class="sxs-lookup"><span data-stu-id="0b2bd-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="0b2bd-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="0b2bd-120">Solution</span></span>

<span data-ttu-id="0b2bd-121">Per avere questa funzionalità in futuro, un utente dovrà installare un'applicazione simile da Microsoft o da un altro fornitore di software.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



