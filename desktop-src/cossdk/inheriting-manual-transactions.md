---
description: Eredità di transazioni manuali
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Eredità di transazioni manuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304615"
---
# <a name="inheriting-manual-transactions"></a><span data-ttu-id="49997-103">Eredità di transazioni manuali</span><span class="sxs-lookup"><span data-stu-id="49997-103">Inheriting Manual Transactions</span></span>

<span data-ttu-id="49997-104">Se un oggetto con una transazione BYOT nel contesto crea un secondo oggetto, l'oggetto downstream può ereditare la transazione BYOT (se configurata per ereditare le transazioni).</span><span class="sxs-lookup"><span data-stu-id="49997-104">If an object with a BYOT transaction in its context creates a second object, the downstream object can inherit the BYOT transaction (if configured to inherit transactions).</span></span> <span data-ttu-id="49997-105">Il primo oggetto creato con il gateway BYOT deve essere configurato per le transazioni "require" o "Support".</span><span class="sxs-lookup"><span data-stu-id="49997-105">The first object created using the BYOT gateway needs to be configured to "require" or "support" transactions.</span></span> <span data-ttu-id="49997-106">Gli oggetti successivi nell'attività possono essere configurati in base ai requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="49997-106">Subsequent objects in the activity could be configured based on application requirements.</span></span>

<span data-ttu-id="49997-107">Per le transazioni automatiche, il runtime COM+ non tenta di eseguire il commit della transazione fino a quando l'oggetto radice non indica che è pronto (chiamando il [**completamento**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) prima di tornare da una chiamata).</span><span class="sxs-lookup"><span data-stu-id="49997-107">For automatic transactions, the COM+ runtime does not attempt to commit the transaction until the root object indicates that it is ready (by calling [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) before returning from a call).</span></span> <span data-ttu-id="49997-108">Gli utenti devono tenere presente che una transazione BYOT potrebbe eseguire il commit in modo anomalo (in quanto il lavoro degli oggetti figlio non è stato completato), perché la "radice" non è in esecuzione nell'ambiente di runtime COM+ e la semantica di commit non è associata alla durata dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="49997-108">Users should be aware that a BYOT transaction could commit prematurely (in that the work of child objects has not been completed), because the "root" is not running under the COM+ runtime environment, and the commit semantics are not tied to the lifetime of the object.</span></span> <span data-ttu-id="49997-109">In generale, l'utente deve prestare attenzione a non violare il limite di sincronizzazione della transazione.</span><span class="sxs-lookup"><span data-stu-id="49997-109">In general, the user should take care to not violate the synchronization boundary of the transaction.</span></span>

<span data-ttu-id="49997-110">In caso contrario, viene applicata la semantica di commit COM+.</span><span class="sxs-lookup"><span data-stu-id="49997-110">Otherwise, COM+ commit semantics apply.</span></span> <span data-ttu-id="49997-111">COM+ non tenterà di eseguire il commit di una transazione mentre è in corso una chiamata a un oggetto all'interno di un limite di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="49997-111">COM+ will not attempt to commit a transaction while an object within a synchronization boundary is in call.</span></span> <span data-ttu-id="49997-112">Gli oggetti possono inoltre indicare la loro coerenza usando [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span><span class="sxs-lookup"><span data-stu-id="49997-112">Also, objects can indicate their consistency using [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit).</span></span> <span data-ttu-id="49997-113">Se viene effettuato un tentativo di eseguire il commit di una transazione che include il lavoro di un oggetto denominato **DisableCommit**, la transazione verrà interrotta.</span><span class="sxs-lookup"><span data-stu-id="49997-113">If an attempt is made to commit a transaction which includes the work of an object that has called **DisableCommit**, the transaction will abort.</span></span>

 

 



