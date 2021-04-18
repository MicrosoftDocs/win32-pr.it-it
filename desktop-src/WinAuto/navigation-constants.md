---
title: Costanti di navigazione (oleacc. h)
description: In questo argomento vengono descritti i valori costanti, definiti in oleacc. h, che indicano la direzione spaziale (su, giù, sinistra e destra) o logica (prima figlio, ultima, successiva e precedente) osservata quando i client utilizzano IAccessible accNavigate per spostarsi da un elemento dell'interfaccia utente all'altro nello stesso contenitore.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327476"
---
# <a name="navigation-constants"></a><span data-ttu-id="f1c94-103">Costanti di navigazione</span><span class="sxs-lookup"><span data-stu-id="f1c94-103">Navigation Constants</span></span>

<span data-ttu-id="f1c94-104">In questo argomento vengono descritti i valori costanti, definiti in oleacc. h, che indicano la direzione *spaziale* (su, giù, sinistra e destra) o *logica* (prima figlio, ultima, successiva e precedente) osservata quando i client utilizzano [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) per spostarsi da un elemento dell'interfaccia utente a un altro nello stesso contenitore.</span><span class="sxs-lookup"><span data-stu-id="f1c94-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="f1c94-105">Per ulteriori informazioni, vedere [proprietà e metodi di navigazione degli oggetti](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f1c94-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="f1c94-106">Le costanti di navigazione di Microsoft Active Accessibility sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1c94-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="f1c94-107">Costante</span><span class="sxs-lookup"><span data-stu-id="f1c94-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="f1c94-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1c94-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="f1c94-109"><dt>**NAVDIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="f1c94-110">Passare all'oggetto di pari livello posizionato sotto l'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="f1c94-111"><dt>**NAVDIR \_ FIRSTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="f1c94-112">Passa al primo elemento figlio di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c94-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="f1c94-113">Quando si usa questo flag, il membro **LVAL** del parametro *VARSTART* deve essere CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="f1c94-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="f1c94-114"><dt>**\_LastChild NAVDIR**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="f1c94-115">Passa all'ultimo elemento figlio di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f1c94-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="f1c94-116">Quando si usa questo flag, il membro **LVAL** del parametro *VARSTART* deve essere CHILDID \_ self.</span><span class="sxs-lookup"><span data-stu-id="f1c94-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="f1c94-117"><dt>**NAVDIR a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="f1c94-118">Passare all'oggetto di pari livello che si trova a sinistra dell'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="f1c94-119"><dt>**NAVDIR \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="f1c94-120">Passare al successivo oggetto logico; in genere, è un elemento di pari livello dell'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="f1c94-121"><dt>**NAVDIR \_ precedente**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="f1c94-122">Passare all'oggetto logico precedente; in genere, è un elemento di pari livello dell'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="f1c94-123"><dt>**NAVDIR a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="f1c94-124">Passare all'oggetto di pari livello che si trova a destra dell'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="f1c94-125"><dt>**NAVDIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="f1c94-126">Passare all'oggetto di pari livello posizionato sopra l'oggetto iniziale.</span><span class="sxs-lookup"><span data-stu-id="f1c94-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="f1c94-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1c94-127">Requirements</span></span>



| <span data-ttu-id="f1c94-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c94-128">Requirement</span></span> | <span data-ttu-id="f1c94-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f1c94-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c94-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1c94-130">Header</span></span><br/> | <dl> <span data-ttu-id="f1c94-131"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c94-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





