---
description: ICE28 viene in genere usato per verificare che l'azione ForceReboot venga posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azione. Vedere l'argomento azione ForceReboot per determinare le azioni che compongono questo gruppo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750130"
---
# <a name="ice28"></a><span data-ttu-id="fe309-104">ICE28</span><span class="sxs-lookup"><span data-stu-id="fe309-104">ICE28</span></span>

<span data-ttu-id="fe309-105">ICE28 viene in genere usato per verificare che l'azione ForceReboot venga posizionata prima o dopo e mai all'interno di un gruppo specifico di azioni nelle tabelle della sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="fe309-105">ICE28 is commonly used to validate that the ForceReboot action is placed before or after, and never within, a specific group of actions in the action sequence tables.</span></span> <span data-ttu-id="fe309-106">Vedere l'argomento [azione ForceReboot](forcereboot-action.md) per determinare le azioni che compongono questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="fe309-106">See the [ForceReboot action](forcereboot-action.md) topic to determine the actions that comprise this group.</span></span>

<span data-ttu-id="fe309-107">ICE28 convalida le azioni nelle tabelle di sequenza seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe309-107">ICE28 validates actions in the following sequence tables:</span></span>

[<span data-ttu-id="fe309-108">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="fe309-108">AdminUISequence table</span></span>](adminuisequence-table.md)

[<span data-ttu-id="fe309-109">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="fe309-109">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)

[<span data-ttu-id="fe309-110">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="fe309-110">InstallUISequence table</span></span>](installuisequence-table.md)

[<span data-ttu-id="fe309-111">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="fe309-111">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="fe309-112">Risultato</span><span class="sxs-lookup"><span data-stu-id="fe309-112">Result</span></span>

<span data-ttu-id="fe309-113">ICE28 Invia un messaggio di errore se ForceReboot viene sequenziato all'interno del gruppo di azioni specificato.</span><span class="sxs-lookup"><span data-stu-id="fe309-113">ICE28 posts an error message if ForceReboot is sequenced within the specified action group.</span></span>

## <a name="example"></a><span data-ttu-id="fe309-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe309-114">Example</span></span>

<span data-ttu-id="fe309-115">Per l'esempio illustrato, ICE28 invia il messaggio di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="fe309-115">For the example shown, ICE28 posts the following error message:</span></span>

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[<span data-ttu-id="fe309-116">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="fe309-116">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="fe309-117">Azione</span><span class="sxs-lookup"><span data-stu-id="fe309-117">Action</span></span>             | <span data-ttu-id="fe309-118">Sequenza</span><span class="sxs-lookup"><span data-stu-id="fe309-118">Sequence</span></span> |
|--------------------|----------|
| <span data-ttu-id="fe309-119">ForceReboot</span><span class="sxs-lookup"><span data-stu-id="fe309-119">ForceReboot</span></span>        | <span data-ttu-id="fe309-120">10</span><span class="sxs-lookup"><span data-stu-id="fe309-120">10</span></span>       |
| <span data-ttu-id="fe309-121">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="fe309-121">RegisterMIMEInfo</span></span>   |   <span data-ttu-id="fe309-122">5</span><span class="sxs-lookup"><span data-stu-id="fe309-122">5</span></span>      |
| <span data-ttu-id="fe309-123">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="fe309-123">RegisterProgIdInfo</span></span> | <span data-ttu-id="fe309-124">15</span><span class="sxs-lookup"><span data-stu-id="fe309-124">15</span></span>       |



 

<span data-ttu-id="fe309-125">Il numero di sequenza di 10 specificato per le interruzioni ForceReboot genera l'errore, perché è incluso tra i numeri di sequenza di RegisterMIMEInfo e RegisterProgIdInfo.</span><span class="sxs-lookup"><span data-stu-id="fe309-125">The sequence number of 10 given to ForceReboot breaks generates the error, because it comes between the sequence numbers of RegisterMIMEInfo and RegisterProgIdInfo.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe309-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe309-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe309-127">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="fe309-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



