---
description: ICE08 verifica che la tabella dei componenti non contenga GUID duplicati. Ogni componente deve avere un GUID univoco. Se la tabella dei componenti non esiste, non viene eseguita alcuna convalida.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314243"
---
# <a name="ice08"></a><span data-ttu-id="e0efa-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="e0efa-105">ICE08</span></span>

<span data-ttu-id="e0efa-106">ICE08 verifica che la [tabella dei componenti](component-table.md) non contenga [GUID](guid.md)duplicati.</span><span class="sxs-lookup"><span data-stu-id="e0efa-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="e0efa-107">Ogni componente deve avere un GUID univoco.</span><span class="sxs-lookup"><span data-stu-id="e0efa-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="e0efa-108">Se la tabella dei componenti non esiste, non viene eseguita alcuna convalida.</span><span class="sxs-lookup"><span data-stu-id="e0efa-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="e0efa-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="e0efa-109">Result</span></span>

<span data-ttu-id="e0efa-110">ICE08 Invia un messaggio di errore se due o più voci nella colonna ComponentId della tabella dei componenti contengono lo stesso GUID.</span><span class="sxs-lookup"><span data-stu-id="e0efa-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="e0efa-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0efa-111">Example</span></span>

<span data-ttu-id="e0efa-112">Per l'esempio seguente, ICE08 Invia un messaggio che informa che i componenti rosso e verde presentano GUID duplicati.</span><span class="sxs-lookup"><span data-stu-id="e0efa-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="e0efa-113">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e0efa-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="e0efa-114">Componente</span><span class="sxs-lookup"><span data-stu-id="e0efa-114">Component</span></span> | <span data-ttu-id="e0efa-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="e0efa-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="e0efa-116">Red</span><span class="sxs-lookup"><span data-stu-id="e0efa-116">Red</span></span>       | <span data-ttu-id="e0efa-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="e0efa-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="e0efa-118">Blu</span><span class="sxs-lookup"><span data-stu-id="e0efa-118">Blue</span></span>      | <span data-ttu-id="e0efa-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="e0efa-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="e0efa-120">Green</span><span class="sxs-lookup"><span data-stu-id="e0efa-120">Green</span></span>     | <span data-ttu-id="e0efa-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="e0efa-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="e0efa-122">Per correggere l'errore, modificare uno dei GUID duplicati.</span><span class="sxs-lookup"><span data-stu-id="e0efa-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0efa-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0efa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0efa-124">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e0efa-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



