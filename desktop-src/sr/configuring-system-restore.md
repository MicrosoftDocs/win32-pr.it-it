---
title: Configurazione ripristino configurazione di sistema
description: Ripristino configurazione di sistema utilizza Strumentazione gestione Windows (WMI) per fornire uno script per la configurazione e l'utilizzo delle relative funzionalità. Espone due classi, SystemRestore e SystemRestoreConfig, nello \\ spazio dei nomi predefinito radice.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399264"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="1bf96-104">Configurazione ripristino configurazione di sistema</span><span class="sxs-lookup"><span data-stu-id="1bf96-104">Configuring System Restore</span></span>

<span data-ttu-id="1bf96-105">Ripristino configurazione di sistema utilizza [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) per fornire uno script per la configurazione e l'utilizzo delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1bf96-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="1bf96-106">Espone due classi, [**SystemRestore**](systemrestore.md) e [**SystemRestoreConfig**](systemrestoreconfig.md), nello \\ spazio dei nomi predefinito radice.</span><span class="sxs-lookup"><span data-stu-id="1bf96-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="1bf96-107">La classe [**SystemRestore**](systemrestore.md) fornisce i metodi per le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="1bf96-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="1bf96-108">Disabilitazione e abilitazione del monitoraggio</span><span class="sxs-lookup"><span data-stu-id="1bf96-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="1bf96-109">Elenco di punti di ripristino disponibili</span><span class="sxs-lookup"><span data-stu-id="1bf96-109">Listing available restore points</span></span>
-   <span data-ttu-id="1bf96-110">Avvio di un ripristino nel sistema locale</span><span class="sxs-lookup"><span data-stu-id="1bf96-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="1bf96-111">Recupero dello stato dell'ultimo ripristino di sistema</span><span class="sxs-lookup"><span data-stu-id="1bf96-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="1bf96-112">La classe [**SystemRestoreConfig**](systemrestoreconfig.md) fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata da ripristino configurazione di sistema in ogni unità.</span><span class="sxs-lookup"><span data-stu-id="1bf96-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="1bf96-113">È possibile accedere a entrambe le classi in modalità remota utilizzando tecniche WMI standard.</span><span class="sxs-lookup"><span data-stu-id="1bf96-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="1bf96-114">Per una descrizione completa di WMI, vedere [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="1bf96-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 