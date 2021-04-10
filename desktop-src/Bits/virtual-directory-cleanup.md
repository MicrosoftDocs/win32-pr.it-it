---
title: Pulizia directory virtuale
description: BITS estende le directory virtuali IIS per supportare i caricamenti.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963251"
---
# <a name="virtual-directory-cleanup"></a><span data-ttu-id="ded16-103">Pulizia directory virtuale</span><span class="sxs-lookup"><span data-stu-id="ded16-103">Virtual Directory Cleanup</span></span>

<span data-ttu-id="ded16-104">BITS estende le directory virtuali IIS per supportare i caricamenti.</span><span class="sxs-lookup"><span data-stu-id="ded16-104">BITS extends IIS virtual directories to support uploads.</span></span> <span data-ttu-id="ded16-105">Ogni directory virtuale dispone di una proprietà di timeout della sessione (la proprietà della metabase IIS [BITSSessionTimeout](bits-iis-extension-properties.md) ) che specifica il periodo di tempo in cui il client BITS deve eseguire lo stato di avanzamento del caricamento del file.</span><span class="sxs-lookup"><span data-stu-id="ded16-105">Each virtual directory has a session time-out property (the IIS [BITSSessionTimeout](bits-iis-extension-properties.md) metabase property) that specifies the period of time in which the BITS client must make progress in uploading the file.</span></span> <span data-ttu-id="ded16-106">Se durante tale periodo non viene eseguito alcun avanzamento (il timer viene reimpostato quando viene eseguito lo stato di avanzamento), BITS chiude la sessione.</span><span class="sxs-lookup"><span data-stu-id="ded16-106">If no progress is made during that period (the timer is reset when progress is made), BITS closes the session.</span></span> <span data-ttu-id="ded16-107">Il timeout della sessione predefinito è di 14 giorni.</span><span class="sxs-lookup"><span data-stu-id="ded16-107">The default session time-out is 14 days.</span></span>

<span data-ttu-id="ded16-108">BITS aggiunge un elemento di lavoro al [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per ogni directory virtuale creata e abilitata.</span><span class="sxs-lookup"><span data-stu-id="ded16-108">BITS adds a work item to the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) for each virtual directory you create and enable.</span></span> <span data-ttu-id="ded16-109">L'elemento di lavoro elimina le risorse associate alle sessioni chiuse.</span><span class="sxs-lookup"><span data-stu-id="ded16-109">The work item deletes resources associated with the closed sessions.</span></span> <span data-ttu-id="ded16-110">Per impostazione predefinita, la pulizia viene eseguita ogni 12 ore.</span><span class="sxs-lookup"><span data-stu-id="ded16-110">By default, the cleanup occurs every 12 hours.</span></span> <span data-ttu-id="ded16-111">Se due directory virtuali puntano alla stessa directory fisica, il processo di pulizia avviato da una delle directory Elimina le risorse associate a tutte le sessioni chiuse nella directory fisica.</span><span class="sxs-lookup"><span data-stu-id="ded16-111">If two virtual directories point to the same physical directory, the cleanup process initiated by one of the directories deletes the resources associated with all closed sessions in the physical directory.</span></span>

<span data-ttu-id="ded16-112">Utilizzare la scheda estensione BITS o le interfacce [utilità di pianificazione](/windows/desktop/TaskSchd/task-scheduler-start-page) per modificare la pianificazione della pulizia nel modo appropriato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ded16-112">Use the BITS Extension tab or the [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) interfaces to change the cleanup schedule as appropriate for your application.</span></span> <span data-ttu-id="ded16-113">È anche possibile chiamare il metodo [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) per recuperare un puntatore di interfaccia all'attività di pulizia associata alla directory virtuale.</span><span class="sxs-lookup"><span data-stu-id="ded16-113">You can also call the [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) method to retrieve an interface pointer to the cleanup task associated with the virtual directory.</span></span>

> [!Note]  
> <span data-ttu-id="ded16-114">Se il Utilità di pianificazione viene disabilitato dopo l'abilitazione della directory virtuale, il processo di pulizia della directory virtuale non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="ded16-114">If the Task Scheduler is disabled after the virtual directory is enabled, the virtual directory cleanup process will not work.</span></span>

 

 

 