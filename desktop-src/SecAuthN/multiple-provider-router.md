---
description: Il router multi-provider (MPR) gestisce la comunicazione tra il sistema operativo Windows e i provider di rete installati. Consente a Windows di presentare una rete integrata all'utente.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Router per più provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa7c4e76901c31e3b5dc7f329a23838aba4f7be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883890"
---
# <a name="multiple-provider-router"></a><span data-ttu-id="ff40e-104">Router per più provider</span><span class="sxs-lookup"><span data-stu-id="ff40e-104">Multiple Provider Router</span></span>

<span data-ttu-id="ff40e-105">Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) gestisce la comunicazione tra il sistema operativo Windows e i provider di rete installati.</span><span class="sxs-lookup"><span data-stu-id="ff40e-105">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication between the Windows operating system and the installed network providers.</span></span> <span data-ttu-id="ff40e-106">Consente a Windows di presentare una rete integrata all'utente.</span><span class="sxs-lookup"><span data-stu-id="ff40e-106">It enables Windows to present an integrated network to the user.</span></span>

<span data-ttu-id="ff40e-107">All'avvio di MPR, viene controllato il registro di sistema per determinare quali provider di rete sono installati nel sistema e l'ordine in cui devono essere ciclati.</span><span class="sxs-lookup"><span data-stu-id="ff40e-107">When the MPR starts, it checks the registry to determine which network providers are installed on the system and the order they should be cycled through.</span></span> <span data-ttu-id="ff40e-108">Carica tutte le dll del provider di rete registrate e le usa per elaborare le chiamate WNet successive effettuate dall'interfaccia utente o da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ff40e-108">It loads all registered network provider DLLs and uses them to process subsequent WNet calls made by the user interface or other applications.</span></span>

<span data-ttu-id="ff40e-109">Per ulteriori informazioni sulle funzioni WNet, vedere la pagina relativa alla [rete Windows](../wnet/windows-networking-wnet-.md).</span><span class="sxs-lookup"><span data-stu-id="ff40e-109">For more information about WNet functions, see [Windows Networking](../wnet/windows-networking-wnet-.md).</span></span>

 

 
