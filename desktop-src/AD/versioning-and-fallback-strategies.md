---
title: Strategia di controllo delle versioni e fallback
description: Quando un'applicazione rileva un aggiornamento parziale utilizzando una delle tecniche precedenti o legge un set di oggetti la cui data effettiva non è ancora stata raggiunta, l'applicazione deve gestire la situazione normalmente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- ANNUNCIO sulle strategie di controllo delle versioni e fallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855378"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="d33c4-104">Strategia di controllo delle versioni e fallback</span><span class="sxs-lookup"><span data-stu-id="d33c4-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="d33c4-105">Quando un'applicazione rileva un aggiornamento parziale utilizzando una delle tecniche precedenti o legge un set di oggetti la cui data effettiva non è ancora stata raggiunta, l'applicazione deve gestire la situazione normalmente.</span><span class="sxs-lookup"><span data-stu-id="d33c4-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="d33c4-106">Per alcune applicazioni, la risposta normale consiste nel "eseguire il fallback" a una versione precedente degli oggetti in questione.</span><span class="sxs-lookup"><span data-stu-id="d33c4-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="d33c4-107">Active Directory Domain Services non forniscono una funzionalità di controllo delle versioni: le applicazioni che desiderano questa funzionalità devono fornirle autonomamente.</span><span class="sxs-lookup"><span data-stu-id="d33c4-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="d33c4-108">Gli approcci al controllo delle versioni includono il mantenimento dei valori "ultimi noti" memorizzati nella cache in locale e l'archiviazione di più insiemi di oggetti nella directory, ad esempio nei contenitori "obsoleti", "correnti" e "nuovi".</span><span class="sxs-lookup"><span data-stu-id="d33c4-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="d33c4-109">Sono possibili molti altri schemi.</span><span class="sxs-lookup"><span data-stu-id="d33c4-109">Many other schemes are possible.</span></span>

<span data-ttu-id="d33c4-110">Le implementazioni devono prestare attenzione a evitare conseguenze impreviste.</span><span class="sxs-lookup"><span data-stu-id="d33c4-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="d33c4-111">Una versione precedente degli oggetti deve essere utilizzata solo quando viene rilevato un aggiornamento parziale o i nuovi oggetti non sono ancora "efficaci".</span><span class="sxs-lookup"><span data-stu-id="d33c4-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="d33c4-112">Il fallback perché qualcosa nell'applicazione "non funziona" potrebbe aggirare l'intento di un amministratore.</span><span class="sxs-lookup"><span data-stu-id="d33c4-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="d33c4-113">Ad esempio, due computer che in precedenza potevano comunicare potrebbero non essere in grado di eseguire questa operazione a causa di una modifica nei criteri di Internet Protocol Security (IPsec).</span><span class="sxs-lookup"><span data-stu-id="d33c4-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="d33c4-114">Se questo comportamento è intenzionale per la parte dell'amministratore, i sistemi interessati non devono eseguire il fallback ai criteri che consentivano la comunicazione, perché si tratta di una violazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d33c4-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




