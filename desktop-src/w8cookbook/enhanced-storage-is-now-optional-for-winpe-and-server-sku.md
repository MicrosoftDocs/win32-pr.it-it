---
title: Archiviazione avanzata è ora facoltativa per WINPE e SKU del server
description: Archiviazione avanzata è ora facoltativa per WINPE e SKU del server
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104339423"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a><span data-ttu-id="2e93f-103">Archiviazione avanzata è ora facoltativa per WINPE e SKU del server</span><span class="sxs-lookup"><span data-stu-id="2e93f-103">Enhanced storage is now optional for WINPE and server SKU</span></span>

## <a name="platforms"></a><span data-ttu-id="2e93f-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="2e93f-104">Platforms</span></span>

<span data-ttu-id="2e93f-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e93f-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="2e93f-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e93f-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="2e93f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e93f-107">Description</span></span>

<span data-ttu-id="2e93f-108">Archiviazione avanzata è sempre disponibile nei dispositivi Windows 7 USB.</span><span class="sxs-lookup"><span data-stu-id="2e93f-108">Enhanced storage was always available in Windows 7 USB devices.</span></span> <span data-ttu-id="2e93f-109">Con il rilascio di Windows 8, è disponibile per tutti i dispositivi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e93f-109">With the release of Windows 8, it is available for all storage devices.</span></span> <span data-ttu-id="2e93f-110">Nei dispositivi basati su client, è abilitata per impostazione predefinita; nei dispositivi server è facoltativo e deve essere sottoposta a provisioning tramite Ambiente preinstallazione di Windows (WinPE).</span><span class="sxs-lookup"><span data-stu-id="2e93f-110">In client-based devices, it is enabled by default; in server devices it is optional and must be provisioned through Windows Preinstallation Environment (WinPE).</span></span>

## <a name="manifestation"></a><span data-ttu-id="2e93f-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="2e93f-111">Manifestation</span></span>

<span data-ttu-id="2e93f-112">Il dispositivo server avrà esito negativo se non è abilitata l'archiviazione avanzata.</span><span class="sxs-lookup"><span data-stu-id="2e93f-112">The server device will fail if enhanced storage is not enabled.</span></span>

<span data-ttu-id="2e93f-113">È necessario eseguire il provisioning dei dispositivi di avvio tramite WinPE con questa funzionalità abilitata.</span><span class="sxs-lookup"><span data-stu-id="2e93f-113">Boot devices must be provisioned through WinPE with this enabled.</span></span>

## <a name="solution"></a><span data-ttu-id="2e93f-114">Soluzione</span><span class="sxs-lookup"><span data-stu-id="2e93f-114">Solution</span></span>

<span data-ttu-id="2e93f-115">Poiché l'archiviazione avanzata è facoltativa per il server di runtime, gli sviluppatori devono aggiungerla a WinPE per il provisioning e l'attivazione di tali unità.</span><span class="sxs-lookup"><span data-stu-id="2e93f-115">Because enhanced storage is optional for runtime server, developers must add it to WinPE for provisioning and activation of those drives.</span></span> <span data-ttu-id="2e93f-116">Per informazioni dettagliate, vedere la guida alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2e93f-116">See the deployment guide for details.</span></span>

<span data-ttu-id="2e93f-117">Gli amministratori del server devono quindi configurare in modo esplicito il server per l'utilizzo dell'archiviazione avanzata.</span><span class="sxs-lookup"><span data-stu-id="2e93f-117">Server administrators must then explicitly configure their server to use enhanced storage.</span></span>

 

 




