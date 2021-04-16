---
title: Monitoraggio del sistema
description: Monitoraggio del sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395222"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="dea91-103">Monitoraggio del sistema</span><span class="sxs-lookup"><span data-stu-id="dea91-103">Monitoring the System</span></span>

<span data-ttu-id="dea91-104">Ripristino configurazione di sistema in Windows Vista e in seguito Salva una copia del volume durante la generazione di un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dea91-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="dea91-105">Per ripristino configurazione di sistema sono necessari almeno 300 MB di spazio libero su disco nell'unità di sistema durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dea91-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="dea91-106">Ripristino configurazione di sistema in Windows XP esegue il monitoraggio di un set di base di file di sistema e dell'applicazione, archiviando gli Stati di questi file prima che vengano apportate modifiche al sistema.</span><span class="sxs-lookup"><span data-stu-id="dea91-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="dea91-107">Ripristino configurazione di sistema salva anche uno snapshot completo del registro di sistema e alcuni file di sistema dinamici.</span><span class="sxs-lookup"><span data-stu-id="dea91-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="dea91-108">Per ripristino configurazione di sistema sono necessari almeno 200 MB di spazio libero su disco nell'unità di sistema durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dea91-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="dea91-109">Quando la quantità di spazio libero su disco scende sotto 50 MB in qualsiasi unità, ripristino configurazione di sistema passa alla modalità standby e interrompe la creazione dei punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dea91-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="dea91-110">Tutti i punti di ripristino vengono eliminati in quel momento.</span><span class="sxs-lookup"><span data-stu-id="dea91-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="dea91-111">Ripristino configurazione di sistema riattiva e riprende la creazione di punti di ripristino non appena 200 MB di spazio su disco è disponibile nell'unità di sistema.</span><span class="sxs-lookup"><span data-stu-id="dea91-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="dea91-112">I file monitorati o esclusi dal monitoraggio vengono specificati nel file% windir% \\ system32 \\ restore \\Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="dea91-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="dea91-113">Per altre informazioni, vedere [estensioni di file monitorate](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="dea91-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




