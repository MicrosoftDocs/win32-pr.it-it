---
description: ICE09 verifica che il bit permanente sia impostato per ogni componente contrassegnato per l'installazione in SystemFolder.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cd20a1b354888877be0f5d456b6d6af2bdec82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757631"
---
# <a name="ice09"></a><span data-ttu-id="7c7ba-103">ICE09</span><span class="sxs-lookup"><span data-stu-id="7c7ba-103">ICE09</span></span>

<span data-ttu-id="7c7ba-104">ICE09 verifica che il bit permanente sia impostato per ogni componente contrassegnato per l'installazione in SystemFolder.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-104">ICE09 validates that the permanent bit is set for every component marked for installation into the SystemFolder.</span></span> <span data-ttu-id="7c7ba-105">ICE09 pubblica un avviso perché è consigliabile evitare di installare componenti di sistema non permanenti in SystemFolder.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-105">ICE09 posts a warning because you should avoid installing non-permanent system components to the SystemFolder.</span></span> <span data-ttu-id="7c7ba-106">Per evitare questo avviso, impostare il bit permanente nella colonna attributi della tabella dei [componenti](component-table.md) per ogni componente contrassegnato per l'installazione in SystemFolder.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-106">To prevent this warning, set the Permanent bit in the Attributes column of the [Component table](component-table.md) for every component that is marked for installation into the SystemFolder.</span></span> <span data-ttu-id="7c7ba-107">Se il database non dispone di una tabella dei componenti, non viene eseguita alcuna convalida.</span><span class="sxs-lookup"><span data-stu-id="7c7ba-107">No validation is done if the database does not have a Component table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c7ba-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c7ba-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c7ba-109">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="7c7ba-109">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



