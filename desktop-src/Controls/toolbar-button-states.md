---
title: Stati del pulsante della barra degli strumenti (CommCtrl. h)
description: Questa sezione elenca gli Stati che possono essere presenti in un pulsante della barra degli strumenti.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327591"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="b29c9-103">Stati del pulsante della barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="b29c9-103">Toolbar Button States</span></span>

<span data-ttu-id="b29c9-104">Questa sezione elenca gli Stati che possono essere presenti in un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b29c9-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="b29c9-105">Costante</span><span class="sxs-lookup"><span data-stu-id="b29c9-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="b29c9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b29c9-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="b29c9-107"><dt>**TBSTATE \_ selezionato**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="b29c9-108">Il pulsante ha lo stile di [**\_ controllo TBSTYLE**](toolbar-control-and-button-styles.md) e viene fatto clic su di esso.</span><span class="sxs-lookup"><span data-stu-id="b29c9-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="b29c9-109"><dt>**\_ellissi TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="b29c9-110">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b29c9-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="b29c9-111">Il testo del pulsante è troncato e vengono visualizzati i puntini di sospensione.</span><span class="sxs-lookup"><span data-stu-id="b29c9-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="b29c9-112"><dt>**TBSTATE \_ abilitato**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="b29c9-113">Il pulsante accetta l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b29c9-113">The button accepts user input.</span></span> <span data-ttu-id="b29c9-114">Un pulsante che non dispone di questo stato è disattivato.</span><span class="sxs-lookup"><span data-stu-id="b29c9-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="b29c9-115"><dt>**TBSTATE \_ nascosto**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="b29c9-116">Il pulsante non è visibile e non è in grado di ricevere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b29c9-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="b29c9-117"><dt>**TBSTATE \_ INdeterminato**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="b29c9-118">Il pulsante è disattivato.</span><span class="sxs-lookup"><span data-stu-id="b29c9-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="b29c9-119"><dt>**TBSTATE \_ contrassegnato come**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="b29c9-120">[Versione 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b29c9-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="b29c9-121">Il pulsante è contrassegnato.</span><span class="sxs-lookup"><span data-stu-id="b29c9-121">The button is marked.</span></span> <span data-ttu-id="b29c9-122">L'interpretazione di un elemento contrassegnato dipende dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b29c9-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="b29c9-123"><dt>**TBSTATE \_ premuto**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="b29c9-124">Si fa clic sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="b29c9-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="b29c9-125"><dt>**TBSTATE a \_ capo**</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="b29c9-126">Il pulsante è seguito da un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="b29c9-126">The button is followed by a line break.</span></span> <span data-ttu-id="b29c9-127">Il pulsante deve avere anche lo \_ stato abilitato per TBSTATE.</span><span class="sxs-lookup"><span data-stu-id="b29c9-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="b29c9-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="b29c9-128">Remarks</span></span>

<span data-ttu-id="b29c9-129">Una barra degli strumenti può avere una combinazione di Stati.</span><span class="sxs-lookup"><span data-stu-id="b29c9-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29c9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b29c9-130">Requirements</span></span>



| <span data-ttu-id="b29c9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b29c9-131">Requirement</span></span> | <span data-ttu-id="b29c9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b29c9-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b29c9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b29c9-133">Header</span></span><br/> | <dl> <span data-ttu-id="b29c9-134"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b29c9-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





