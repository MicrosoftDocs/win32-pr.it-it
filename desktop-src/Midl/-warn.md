---
title: opzione/warn
description: L'opzione/warn specifica il livello di avviso del compilatore MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn switch MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718199"
---
# <a name="warn-switch"></a><span data-ttu-id="ceacb-104">opzione/warn</span><span class="sxs-lookup"><span data-stu-id="ceacb-104">/warn switch</span></span>

<span data-ttu-id="ceacb-105">L'opzione **/warn** specifica il livello di avviso del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="ceacb-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="ceacb-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="ceacb-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="ceacb-107">*level*</span><span class="sxs-lookup"><span data-stu-id="ceacb-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="ceacb-108">Specifica il livello di avviso, ovvero un numero intero compreso tra 0 e 4.</span><span class="sxs-lookup"><span data-stu-id="ceacb-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="ceacb-109">Non è presente alcuno spazio tra l'opzione **/warn** e la cifra che indica il valore a livello di avviso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceacb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceacb-110">Remarks</span></span>

<span data-ttu-id="ceacb-111">Il livello di avviso indica la gravità dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="ceacb-112">I livelli di avviso sono compresi tra 1 e 4 e il valore zero indica che non vengono visualizzate informazioni di avviso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="ceacb-113">L'avviso con la massima gravità è il livello 1.</span><span class="sxs-lookup"><span data-stu-id="ceacb-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="ceacb-114">Nella tabella seguente vengono descritti gli avvisi per ogni livello di avviso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="ceacb-115">Livello avvisi</span><span class="sxs-lookup"><span data-stu-id="ceacb-115">Warning level</span></span> | <span data-ttu-id="ceacb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceacb-116">Description</span></span>                                             | <span data-ttu-id="ceacb-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="ceacb-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ceacb-118">0</span><span class="sxs-lookup"><span data-stu-id="ceacb-118">0</span></span>             | <span data-ttu-id="ceacb-119">Nessun avviso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="ceacb-120">1</span><span class="sxs-lookup"><span data-stu-id="ceacb-120">1</span></span>             | <span data-ttu-id="ceacb-121">Avvisi gravi che possono causare errori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ceacb-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="ceacb-122">Nessun handle di binding specificato, puntatori senza attributi, opzioni in conflitto.</span><span class="sxs-lookup"><span data-stu-id="ceacb-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="ceacb-123">2</span><span class="sxs-lookup"><span data-stu-id="ceacb-123">2</span></span>             | <span data-ttu-id="ceacb-124">Potrebbe causare problemi nell'ambiente operativo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ceacb-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="ceacb-125">La lunghezza dell'identificatore supera i 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ceacb-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="ceacb-126">Non è stato specificato alcun ARM di Unione predefinito.</span><span class="sxs-lookup"><span data-stu-id="ceacb-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="ceacb-127">3</span><span class="sxs-lookup"><span data-stu-id="ceacb-127">3</span></span>             | <span data-ttu-id="ceacb-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ceacb-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="ceacb-129">4</span><span class="sxs-lookup"><span data-stu-id="ceacb-129">4</span></span>             | <span data-ttu-id="ceacb-130">Livello di avviso più basso.</span><span class="sxs-lookup"><span data-stu-id="ceacb-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="ceacb-131">Costrutti non ANSI C.</span><span class="sxs-lookup"><span data-stu-id="ceacb-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="ceacb-132">Gli avvisi sono diversi dagli errori.</span><span class="sxs-lookup"><span data-stu-id="ceacb-132">Warnings are different from errors.</span></span> <span data-ttu-id="ceacb-133">Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="ceacb-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="ceacb-134">Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="ceacb-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="ceacb-135">Il livello di avviso impostato dall'opzione **/warn** può essere usato con l'opzione [**WX**](-wx.md) per fare in modo che il compilatore MIDL interrompa l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="ceacb-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="ceacb-136">Il comportamento dell'opzione **/warn** è uguale a quello dell'opzione [**/W**](-w.md) .</span><span class="sxs-lookup"><span data-stu-id="ceacb-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="ceacb-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="ceacb-137">Examples</span></span>

<span data-ttu-id="ceacb-138">**MIDL/warn2 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="ceacb-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="ceacb-139">**MIDL/warn4 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="ceacb-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="ceacb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceacb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceacb-141">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="ceacb-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




