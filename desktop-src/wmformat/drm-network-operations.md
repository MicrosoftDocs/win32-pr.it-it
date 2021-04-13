---
title: Operazioni di rete DRM
description: Operazioni di rete DRM
ms.assetid: 4a10c811-2aa1-4b97-8a72-61e8b04075a8
keywords:
- Windows Media Format SDK, operazioni di rete DRM
- ASF (Advanced Systems Format), operazioni di rete DRM
- ASF (Advanced Systems Format), operazioni di rete DRM
- Digital Rights Management (DRM), operazioni di rete
- DRM (Digital Rights Management), operazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875186e43e066d71847da014468e9b1764b60cf2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328692"
---
# <a name="drm-network-operations"></a><span data-ttu-id="a9318-108">Operazioni di rete DRM</span><span class="sxs-lookup"><span data-stu-id="a9318-108">DRM Network Operations</span></span>

<span data-ttu-id="a9318-109">Per diverse operazioni relative a DRM è necessario che l'applicazione si connetta a un servizio in esecuzione in una rete.</span><span class="sxs-lookup"><span data-stu-id="a9318-109">Several DRM-related operations require your application to connect to a service running on a network.</span></span> <span data-ttu-id="a9318-110">Queste operazioni includono l'individualizzazione, l'acquisizione di licenze, la revoca delle licenze e il backup e il ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="a9318-110">These operations include individualization, license acquisition, license revocation, and license backup and restoration.</span></span>

<span data-ttu-id="a9318-111">Come per qualsiasi transazione di rete, l'applicazione deve tenere conto di una serie di difficoltà quando si includono funzionalità che richiedono operazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="a9318-111">As with any network transaction, your application should account for a variety of difficulties when including features that require network operations.</span></span> <span data-ttu-id="a9318-112">L'applicazione deve tenere traccia dello stato dell'operazione in base a qualsiasi extent possibile per la funzionalità specifica, in genere gestendo i messaggi di stato.</span><span class="sxs-lookup"><span data-stu-id="a9318-112">Your application should track the status of the operation to whatever extent is possible for the specific feature, usually by handling status messages.</span></span> <span data-ttu-id="a9318-113">È necessario fornire un feedback all'utente sullo stato.</span><span class="sxs-lookup"><span data-stu-id="a9318-113">You should provide feedback to the user about status.</span></span> <span data-ttu-id="a9318-114">Se un'operazione non riesce al primo tentativo, è necessario concedere all'utente la possibilità di riprovare.</span><span class="sxs-lookup"><span data-stu-id="a9318-114">If an operation fails on the first try, you should give the user the opportunity to retry.</span></span> <span data-ttu-id="a9318-115">In molti casi, il primo tentativo rileva difficoltà, ma un tentativo successivo viene completato senza errori.</span><span class="sxs-lookup"><span data-stu-id="a9318-115">In many cases, the first attempt encounters difficulty, but a subsequent try completes without error.</span></span>

> [!Note]  
> <span data-ttu-id="a9318-116">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="a9318-116">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a9318-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9318-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9318-118">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="a9318-118">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




