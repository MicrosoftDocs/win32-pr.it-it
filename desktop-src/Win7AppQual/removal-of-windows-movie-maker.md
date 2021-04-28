---
description: Rimozione di Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Rimozione di Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116269"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="b2446-103">Rimozione di Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="b2446-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b2446-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="b2446-104">Affected Platforms</span></span>

<span data-ttu-id="b2446-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2446-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b2446-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2446-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="b2446-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="b2446-107">Feature Impact</span></span>

 <span data-ttu-id="b2446-108">**Gravità** - Alta</span><span class="sxs-lookup"><span data-stu-id="b2446-108">**Severity** - High</span></span>  
<span data-ttu-id="b2446-109">**Frequenza** - Media</span><span class="sxs-lookup"><span data-stu-id="b2446-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="b2446-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2446-110">Description</span></span>

<span data-ttu-id="b2446-111">Microsoft sta deprecando e rimuovendo l'utilità Movie Maker Windows.</span><span class="sxs-lookup"><span data-stu-id="b2446-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="b2446-112">ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b2446-112">This includes:</span></span>

-   <span data-ttu-id="b2446-113">Tutti i punti di ingresso a Windows Movie Maker (ad esempio, Menu Start, Avvio > Esegui)</span><span class="sxs-lookup"><span data-stu-id="b2446-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="b2446-114">Tutti i file binari usati da Windows Movie Maker (tutti gli elementi presenti in %ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="b2446-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="b2446-115">Tuttavia, i file di progetto Movie Maker utente rimarranno nel sistema e saranno accessibili ad altre applicazioni che supportano questo formato di file.</span><span class="sxs-lookup"><span data-stu-id="b2446-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b2446-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="b2446-116">Manifestation</span></span>

<span data-ttu-id="b2446-117">Rimuovere i Movie Maker di Windows nei risultati seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2446-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="b2446-118">Qualsiasi tentativo di avviare Windows Movie Maker con gli argomenti della riga di comando avrà esito negativo</span><span class="sxs-lookup"><span data-stu-id="b2446-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="b2446-119">Tutti i plug-in installati per abilitare nuove trasformazioni e animazioni rimarranno installati, ma non verranno esposti all'utente finale</span><span class="sxs-lookup"><span data-stu-id="b2446-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="b2446-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="b2446-120">Solution</span></span>

<span data-ttu-id="b2446-121">Per avere questa funzionalità in futuro, un utente dovrà installare un'applicazione simile da Microsoft o da un altro provider di software.</span><span class="sxs-lookup"><span data-stu-id="b2446-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



