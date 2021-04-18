---
title: Opzione/W
description: L'opzione/W specifica il livello di avviso del compilatore MIDL. Il livello di avviso indica la gravità dell'avviso.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W switch MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299169"
---
# <a name="w-switch"></a><span data-ttu-id="034e6-105">Opzione/W</span><span class="sxs-lookup"><span data-stu-id="034e6-105">/W switch</span></span>

<span data-ttu-id="034e6-106">L'opzione **/W** specifica il livello di avviso del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="034e6-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="034e6-107">Il livello di avviso indica la gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="034e6-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="034e6-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="034e6-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="034e6-109">*level*</span><span class="sxs-lookup"><span data-stu-id="034e6-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="034e6-110">Specifica il livello di avviso, ovvero un numero intero compreso tra 0 e 4.</span><span class="sxs-lookup"><span data-stu-id="034e6-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="034e6-111">Non è presente alcuno spazio tra l'opzione **/W** e la cifra che indica il valore a livello di avviso.</span><span class="sxs-lookup"><span data-stu-id="034e6-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="034e6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="034e6-112">Remarks</span></span>

<span data-ttu-id="034e6-113">I livelli di avviso sono compresi tra 1 e 4 e il valore zero indica che non vengono visualizzate informazioni di avviso.</span><span class="sxs-lookup"><span data-stu-id="034e6-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="034e6-114">L'avviso con la massima gravità è il livello 1.</span><span class="sxs-lookup"><span data-stu-id="034e6-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="034e6-115">Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.</span><span class="sxs-lookup"><span data-stu-id="034e6-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="034e6-116">Livello avvisi</span><span class="sxs-lookup"><span data-stu-id="034e6-116">Warning level</span></span> | <span data-ttu-id="034e6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="034e6-117">Description</span></span>                                             | <span data-ttu-id="034e6-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="034e6-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="034e6-119">W0</span><span class="sxs-lookup"><span data-stu-id="034e6-119">W0</span></span>            | <span data-ttu-id="034e6-120">Nessun avviso.</span><span class="sxs-lookup"><span data-stu-id="034e6-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="034e6-121">W1</span><span class="sxs-lookup"><span data-stu-id="034e6-121">W1</span></span>            | <span data-ttu-id="034e6-122">Avvisi gravi che possono causare errori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="034e6-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="034e6-123">Nessun handle di binding specificato, puntatori senza attributi, opzioni in conflitto.</span><span class="sxs-lookup"><span data-stu-id="034e6-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="034e6-124">W2</span><span class="sxs-lookup"><span data-stu-id="034e6-124">W2</span></span>            | <span data-ttu-id="034e6-125">Potrebbe causare problemi nell'ambiente operativo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="034e6-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="034e6-126">La lunghezza dell'identificatore supera i 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="034e6-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="034e6-127">Non è stato specificato alcun ARM di Unione predefinito.</span><span class="sxs-lookup"><span data-stu-id="034e6-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="034e6-128">W3</span><span class="sxs-lookup"><span data-stu-id="034e6-128">W3</span></span>            | <span data-ttu-id="034e6-129">Riservato.</span><span class="sxs-lookup"><span data-stu-id="034e6-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="034e6-130">W4</span><span class="sxs-lookup"><span data-stu-id="034e6-130">W4</span></span>            | <span data-ttu-id="034e6-131">Livello di avviso più basso.</span><span class="sxs-lookup"><span data-stu-id="034e6-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="034e6-132">Costrutti non ANSI C.</span><span class="sxs-lookup"><span data-stu-id="034e6-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="034e6-133">Gli avvisi sono diversi dagli errori.</span><span class="sxs-lookup"><span data-stu-id="034e6-133">Warnings are different from errors.</span></span> <span data-ttu-id="034e6-134">Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="034e6-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="034e6-135">Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="034e6-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="034e6-136">Il livello di avviso impostato dall'opzione **/W** può essere usato con l'opzione [**/WX**](-wx.md) per fare in modo che il compilatore MIDL interrompa l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="034e6-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="034e6-137">Il comportamento dell'opzione **/W** è uguale a quello dell'opzione [**/warn**](-warn.md) .</span><span class="sxs-lookup"><span data-stu-id="034e6-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="034e6-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="034e6-138">Examples</span></span>

<span data-ttu-id="034e6-139">**MIDL/W2 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="034e6-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="034e6-140">**MIDL/W4 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="034e6-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="034e6-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="034e6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034e6-142">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="034e6-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="034e6-143">**/warn**</span><span class="sxs-lookup"><span data-stu-id="034e6-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




