---
description: La tabella LaunchCondition viene utilizzata dall'azione LaunchConditions. Contiene un elenco di condizioni che devono essere soddisfatte per poter iniziare l'installazione.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabella LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307255"
---
# <a name="launchcondition-table"></a><span data-ttu-id="033c5-104">Tabella LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="033c5-104">LaunchCondition Table</span></span>

<span data-ttu-id="033c5-105">La tabella LaunchCondition viene utilizzata dall' [azione LaunchConditions](launchconditions-action.md).</span><span class="sxs-lookup"><span data-stu-id="033c5-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="033c5-106">Contiene un elenco di condizioni che devono essere soddisfatte per poter iniziare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="033c5-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="033c5-107">La tabella LaunchCondition include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="033c5-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="033c5-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="033c5-108">Column</span></span>      | <span data-ttu-id="033c5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="033c5-109">Type</span></span>                       | <span data-ttu-id="033c5-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="033c5-110">Key</span></span> | <span data-ttu-id="033c5-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="033c5-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="033c5-112">Condizione</span><span class="sxs-lookup"><span data-stu-id="033c5-112">Condition</span></span>   | [<span data-ttu-id="033c5-113">Condition</span><span class="sxs-lookup"><span data-stu-id="033c5-113">Condition</span></span>](condition.md) | <span data-ttu-id="033c5-114">S</span><span class="sxs-lookup"><span data-stu-id="033c5-114">Y</span></span>   | <span data-ttu-id="033c5-115">N</span><span class="sxs-lookup"><span data-stu-id="033c5-115">N</span></span>        |
| <span data-ttu-id="033c5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="033c5-116">Description</span></span> | [<span data-ttu-id="033c5-117">Formattato</span><span class="sxs-lookup"><span data-stu-id="033c5-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="033c5-118">N</span><span class="sxs-lookup"><span data-stu-id="033c5-118">N</span></span>   | <span data-ttu-id="033c5-119">N</span><span class="sxs-lookup"><span data-stu-id="033c5-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="033c5-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="033c5-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="033c5-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione</span><span class="sxs-lookup"><span data-stu-id="033c5-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="033c5-122">Espressione che deve restituire true per iniziare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="033c5-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="033c5-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="033c5-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="033c5-124">Testo localizzabile da visualizzare quando la condizione ha esito negativo e l'installazione deve essere terminata.</span><span class="sxs-lookup"><span data-stu-id="033c5-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="033c5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="033c5-125">Remarks</span></span>

<span data-ttu-id="033c5-126">Non è possibile garantire l'ordine di valutazione delle condizioni di avvio mediante la creazione della tabella.</span><span class="sxs-lookup"><span data-stu-id="033c5-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="033c5-127">Se è necessario controllare l'ordine in cui vengono valutate le condizioni, è necessario eseguire questa operazione usando il tipo di azione personalizzata 19 azioni personalizzate nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="033c5-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="033c5-128">Convalida</span><span class="sxs-lookup"><span data-stu-id="033c5-128">Validation</span></span>

<dl>

[<span data-ttu-id="033c5-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="033c5-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="033c5-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="033c5-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="033c5-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="033c5-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="033c5-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="033c5-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="033c5-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="033c5-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



