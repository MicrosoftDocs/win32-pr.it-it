---
description: I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento. Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Come utilizzare il modello di selezione dei verbi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979575"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="bbb0b-104">Come utilizzare il modello di selezione dei verbi</span><span class="sxs-lookup"><span data-stu-id="bbb0b-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="bbb0b-105">I valori del registro di sistema devono essere impostati per i verbi per gestire le situazioni in cui un utente può selezionare un singolo elemento, più elementi o una selezione da un elemento.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="bbb0b-106">Un verbo richiede valori di registro distinti per ognuna di queste tre situazioni supportate dal verbo.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="bbb0b-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="bbb0b-107">Instructions</span></span>


<span data-ttu-id="bbb0b-108">Specificare il valore MultiSelectModel per tutti i verbi.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="bbb0b-109">Se il valore MultiSelectModel non è specificato, viene dedotto dal tipo di implementazione del verbo scelto.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="bbb0b-110">Per i metodi basati su COM, ad esempio DropTarget e ExecuteCommand, viene utilizzato il **lettore** e per gli altri metodi viene utilizzato il **documento** .</span><span class="sxs-lookup"><span data-stu-id="bbb0b-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="bbb0b-111">I valori possibili per il modello di selezione dei verbi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbb0b-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="bbb0b-112">Specificare **Single** per i verbi che supportano una sola selezione.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="bbb0b-113">Specificare il **lettore** per i verbi che supportano un numero qualsiasi di elementi.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="bbb0b-114">Specificare il **documento** per i verbi che creano una finestra di primo livello per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="bbb0b-115">Questa operazione limita il numero di elementi attivati e consente di evitare l'esaurimento delle risorse di sistema se l'utente apre troppe finestre.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb0b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbb0b-116">Remarks</span></span>

<span data-ttu-id="bbb0b-117">Quando il numero di elementi selezionati non corrisponde al modello di selezione dei verbi o è maggiore dei limiti predefiniti indicati nella tabella seguente, il verbo non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="bbb0b-118">Tipo di implementazione del verbo</span><span class="sxs-lookup"><span data-stu-id="bbb0b-118">Type of verb implementation</span></span> | <span data-ttu-id="bbb0b-119">Documento</span><span class="sxs-lookup"><span data-stu-id="bbb0b-119">Document</span></span> | <span data-ttu-id="bbb0b-120">Lettore</span><span class="sxs-lookup"><span data-stu-id="bbb0b-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="bbb0b-121">Legacy</span><span class="sxs-lookup"><span data-stu-id="bbb0b-121">Legacy</span></span>                      | <span data-ttu-id="bbb0b-122">15 elementi</span><span class="sxs-lookup"><span data-stu-id="bbb0b-122">15 items</span></span> | <span data-ttu-id="bbb0b-123">100 elementi</span><span class="sxs-lookup"><span data-stu-id="bbb0b-123">100 items</span></span> |
| <span data-ttu-id="bbb0b-124">COM</span><span class="sxs-lookup"><span data-stu-id="bbb0b-124">COM</span></span>                         | <span data-ttu-id="bbb0b-125">15 elementi</span><span class="sxs-lookup"><span data-stu-id="bbb0b-125">15 items</span></span> | <span data-ttu-id="bbb0b-126">Nessun limite</span><span class="sxs-lookup"><span data-stu-id="bbb0b-126">No limit</span></span>  |



 

<span data-ttu-id="bbb0b-127">Di seguito sono riportate voci del registro di sistema di esempio che utilizzano il valore MultiSelectModel.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



