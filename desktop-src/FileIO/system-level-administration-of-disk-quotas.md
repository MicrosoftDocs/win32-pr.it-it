---
description: L'amministratore di sistema può impostare le quote per utenti specifici in un volume. L'amministratore può inoltre impostare le quote predefinite per il volume.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Amministrazione a livello di sistema di quote disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226260"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="f1938-104">Amministrazione a livello di sistema di quote disco</span><span class="sxs-lookup"><span data-stu-id="f1938-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="f1938-105">L'amministratore di sistema può impostare le quote per utenti specifici in un volume.</span><span class="sxs-lookup"><span data-stu-id="f1938-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="f1938-106">L'amministratore può inoltre impostare le quote predefinite per il volume.</span><span class="sxs-lookup"><span data-stu-id="f1938-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="f1938-107">Un nuovo utente del volume riceve la quota predefinita, a meno che l'amministratore non abbia stabilito una quota specifica per tale utente.</span><span class="sxs-lookup"><span data-stu-id="f1938-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="f1938-108">L'amministratore può eseguire una query sul livello di rilevamento e imposizione delle quote (o Stati delle quote), i limiti di quota predefiniti e le informazioni sulla quota per utente.</span><span class="sxs-lookup"><span data-stu-id="f1938-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="f1938-109">Le informazioni sulla quota per utente contengono il limite di quota hardware dell'utente, la soglia di avviso e l'utilizzo della quota.</span><span class="sxs-lookup"><span data-stu-id="f1938-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="f1938-110">L'amministratore può anche abilitare o disabilitare l'imposizione delle quote.</span><span class="sxs-lookup"><span data-stu-id="f1938-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="f1938-111">Sono disponibili tre stati di quota, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f1938-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="f1938-112">State</span><span class="sxs-lookup"><span data-stu-id="f1938-112">State</span></span>          | <span data-ttu-id="f1938-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1938-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1938-114">Quota disabilitata</span><span class="sxs-lookup"><span data-stu-id="f1938-114">Quota disabled</span></span> | <span data-ttu-id="f1938-115">Le modifiche all'utilizzo della quota non vengono rilevate, ma i limiti della quota non vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="f1938-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="f1938-116">In questo stato le prestazioni non sono influenzate dalle quote disco.</span><span class="sxs-lookup"><span data-stu-id="f1938-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="f1938-117">Questo è lo stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="f1938-117">This is the default state.</span></span>                         |
| <span data-ttu-id="f1938-118">Quota rilevata</span><span class="sxs-lookup"><span data-stu-id="f1938-118">Quota tracked</span></span>  | <span data-ttu-id="f1938-119">Le modifiche all'utilizzo della quota vengono rilevate, ma non vengono applicati limiti di quota.</span><span class="sxs-lookup"><span data-stu-id="f1938-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="f1938-120">In questo stato non viene generato alcun evento di violazione della quota e non vengono eseguite operazioni sui file a causa di violazioni della quota del disco.</span><span class="sxs-lookup"><span data-stu-id="f1938-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="f1938-121">Quota applicata</span><span class="sxs-lookup"><span data-stu-id="f1938-121">Quota enforced</span></span> | <span data-ttu-id="f1938-122">Vengono rilevate le modifiche all'utilizzo della quota e vengono applicati i limiti delle quote.</span><span class="sxs-lookup"><span data-stu-id="f1938-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



