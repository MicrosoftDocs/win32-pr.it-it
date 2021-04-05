---
description: I tipi di formato integer dei dati configurabili possono essere utilizzati nei campi di database di tipo text o Integer. L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo. Null non è mai un valore valido per questo tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipi di formato Integer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757034"
---
# <a name="integer-format-types"></a><span data-ttu-id="efacf-105">Tipi di formato Integer</span><span class="sxs-lookup"><span data-stu-id="efacf-105">Integer Format Types</span></span>

<span data-ttu-id="efacf-106">I tipi di formato integer dei dati configurabili possono essere utilizzati nei campi di database di tipo text o Integer.</span><span class="sxs-lookup"><span data-stu-id="efacf-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="efacf-107">L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo.</span><span class="sxs-lookup"><span data-stu-id="efacf-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="efacf-108">Null non è mai un valore valido per questo tipo.</span><span class="sxs-lookup"><span data-stu-id="efacf-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="efacf-109">Il tipo di formato integer seguente esiste.</span><span class="sxs-lookup"><span data-stu-id="efacf-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="efacf-110">Tipo Integer arbitrario</span><span class="sxs-lookup"><span data-stu-id="efacf-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="efacf-111">Gli elementi configurabili del tipo di formato integer vengono utilizzati in colonne di tipo text o Integer e in generale potrebbero essere sostituiti da qualsiasi numero intero positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="efacf-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="efacf-112">Tuttavia, particolari elementi configurabili possono anche avere restrizioni semantiche caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="efacf-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="efacf-113">Un particolare elemento configurabile, ad esempio, deve essere un numero intero compreso tra 0 e 100 e una restrizione semantica aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="efacf-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="efacf-114">Tali restrizioni non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato integer specificato.</span><span class="sxs-lookup"><span data-stu-id="efacf-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



