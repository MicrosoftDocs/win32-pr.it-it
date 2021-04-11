---
description: Aggiungere un record alla tabella CustomAction per l'azione di avvio personalizzata.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Aggiunta dell'avvio alle tabelle CustomAction e binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131506"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="594f1-103">Aggiunta dell'avvio alle tabelle CustomAction e binarie</span><span class="sxs-lookup"><span data-stu-id="594f1-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="594f1-104">Aggiungere un record alla [tabella CustomAction](customaction-table.md) per l'azione di avvio personalizzata.</span><span class="sxs-lookup"><span data-stu-id="594f1-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="594f1-105">Immettere il nome dell'azione personalizzata nella colonna azione della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="594f1-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="594f1-106">Immettere il tipo numerico totale per Launch, 65, nella colonna Type della tabella delle azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="594f1-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="594f1-107">La colonna di origine della tabella CustomAction specifica una chiave nel record della [tabella binaria](binary-table.md) che contiene i dati binari per la dll.</span><span class="sxs-lookup"><span data-stu-id="594f1-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="594f1-108">Immettere Tutorial.dll nella colonna origine della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="594f1-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="594f1-109">Il punto di ingresso specificato nel campo di destinazione della tabella CustomAction deve corrispondere a quello esportato dalla DLL.</span><span class="sxs-lookup"><span data-stu-id="594f1-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="594f1-110">Immettere LaunchTutorial nella colonna destinazione della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="594f1-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="594f1-111">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="594f1-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="594f1-112">Azione</span><span class="sxs-lookup"><span data-stu-id="594f1-112">Action</span></span> | <span data-ttu-id="594f1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="594f1-113">Type</span></span> | <span data-ttu-id="594f1-114">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="594f1-114">Source</span></span>       | <span data-ttu-id="594f1-115">Destinazione</span><span class="sxs-lookup"><span data-stu-id="594f1-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="594f1-116">Launch</span><span class="sxs-lookup"><span data-stu-id="594f1-116">Launch</span></span> | <span data-ttu-id="594f1-117">65</span><span class="sxs-lookup"><span data-stu-id="594f1-117">65</span></span>   | <span data-ttu-id="594f1-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="594f1-118">Tutorial.dll</span></span> | <span data-ttu-id="594f1-119">LaunchTutorial</span><span class="sxs-lookup"><span data-stu-id="594f1-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="594f1-120">Aggiungere la Tutorial.dll creata da tutorial. cpp come flusso binario alla tabella binaria.</span><span class="sxs-lookup"><span data-stu-id="594f1-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="594f1-121">Tabella binaria</span><span class="sxs-lookup"><span data-stu-id="594f1-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="594f1-122">Nome</span><span class="sxs-lookup"><span data-stu-id="594f1-122">Name</span></span>         | <span data-ttu-id="594f1-123">Data</span><span class="sxs-lookup"><span data-stu-id="594f1-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="594f1-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="594f1-124">Tutorial.dll</span></span> | <span data-ttu-id="594f1-125">{*dati binari aggiunti per la dll*}</span><span class="sxs-lookup"><span data-stu-id="594f1-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="594f1-126">Continuare ad [aggiungere un evento di controllo alla fine dell'installazione per eseguire l'avvio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="594f1-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



