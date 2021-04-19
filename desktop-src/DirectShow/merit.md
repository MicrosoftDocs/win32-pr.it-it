---
description: I valori di Merit definiscono l'ordine in cui il gestore del grafico del filtro tenta di aggiungere filtri durante la compilazione del grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Merit (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323989"
---
# <a name="merit"></a><span data-ttu-id="33fe6-103">Merito</span><span class="sxs-lookup"><span data-stu-id="33fe6-103">Merit</span></span>

<span data-ttu-id="33fe6-104">I valori di Merit definiscono l'ordine in cui il gestore del grafico del filtro tenta di aggiungere filtri durante la compilazione del grafo.</span><span class="sxs-lookup"><span data-stu-id="33fe6-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="33fe6-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>Il **merito \_ Preferenza** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **Merit \_ Normal** (0x600000) Merit <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improbabile** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **Merit non \_ \_ \_ use** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **Merit \_ SW \_** Compressor (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **Merit \_ HW \_ Compressor** (0x100050)</span><span class="sxs-lookup"><span data-stu-id="33fe6-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="33fe6-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="33fe6-106">Remarks</span></span>

<span data-ttu-id="33fe6-107">Ogni filtro viene registrato con un valore Merit.</span><span class="sxs-lookup"><span data-stu-id="33fe6-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="33fe6-108">Quando il gestore del grafico dei filtri compila un grafo, enumera tutti i filtri registrati con il tipo di supporto corretto.</span><span class="sxs-lookup"><span data-stu-id="33fe6-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="33fe6-109">Quindi, le tentano in ordine di merito, dal più alto al più basso.</span><span class="sxs-lookup"><span data-stu-id="33fe6-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="33fe6-110">Usa criteri aggiuntivi per scegliere tra i filtri con uguale Merit. Non tenta mai i filtri con un valore Merit minore o uguale a **Merit \_ non \_ \_ usare**.</span><span class="sxs-lookup"><span data-stu-id="33fe6-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="33fe6-111">Un filtro che non deve mai essere considerato per la riproduzione ordinaria deve avere un merito di **merito non \_ \_ \_ usare** o meno.</span><span class="sxs-lookup"><span data-stu-id="33fe6-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="33fe6-112">I filtri possono essere registrati con valori intermedi non definiti da questa enumerazione, ad esempio **Merit \_ Normal** + 1.</span><span class="sxs-lookup"><span data-stu-id="33fe6-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="33fe6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33fe6-113">Requirements</span></span>



| <span data-ttu-id="33fe6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33fe6-114">Requirement</span></span> | <span data-ttu-id="33fe6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="33fe6-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33fe6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33fe6-116">Header</span></span><br/> | <dl> <span data-ttu-id="33fe6-117"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="33fe6-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33fe6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33fe6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fe6-119">Costanti e GUID</span><span class="sxs-lookup"><span data-stu-id="33fe6-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="33fe6-120">Linee guida per la registrazione dei filtri</span><span class="sxs-lookup"><span data-stu-id="33fe6-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="33fe6-121">Connessione intelligente</span><span class="sxs-lookup"><span data-stu-id="33fe6-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




