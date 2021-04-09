---
title: Opzione/WX
description: L'opzione/WX indica al compilatore MIDL di gestire tutti gli errori al livello di avviso specificato come errori.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX switch MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857502"
---
# <a name="wx-switch"></a><span data-ttu-id="3096a-104">Opzione/WX</span><span class="sxs-lookup"><span data-stu-id="3096a-104">/WX switch</span></span>

<span data-ttu-id="3096a-105">L'opzione **/WX** indica al compilatore MIDL di gestire tutti gli errori al livello di avviso specificato come errori.</span><span class="sxs-lookup"><span data-stu-id="3096a-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="3096a-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="3096a-106">Switch Options</span></span>

<span data-ttu-id="3096a-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="3096a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3096a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3096a-108">Remarks</span></span>

<span data-ttu-id="3096a-109">Se si specifica l'opzione **/WX** e non si specifica l'opzione [**/W**](-w.md)*n* , tutti gli avvisi a livello predefinito, livello 1, vengono considerati errori.</span><span class="sxs-lookup"><span data-stu-id="3096a-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="3096a-110">L'opzione [**/W**](-w.md)*n* indica al compilatore di visualizzare tutti gli avvisi a livello *n* e **/WX** indirizza il compilatore alla gestione di tutti gli avvisi come errori.</span><span class="sxs-lookup"><span data-stu-id="3096a-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="3096a-111">La combinazione di queste due opzioni indica al compilatore di gestire tutti gli avvisi a livello *n* come errori.</span><span class="sxs-lookup"><span data-stu-id="3096a-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="3096a-112">Gli errori sono diversi dagli avvisi.</span><span class="sxs-lookup"><span data-stu-id="3096a-112">Errors are different from warnings.</span></span> <span data-ttu-id="3096a-113">Gli errori fanno sì che il compilatore MIDL interrompa l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="3096a-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="3096a-114">Avvisi il compilatore MIDL genera un messaggio informativo e continua l'elaborazione del file IDL.</span><span class="sxs-lookup"><span data-stu-id="3096a-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="3096a-115">Avviso-livello zero (0) indica al compilatore MIDL di non visualizzare le informazioni di avviso.</span><span class="sxs-lookup"><span data-stu-id="3096a-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="3096a-116">Quando le opzioni **/W0** e **/WX** vengono combinate, il compilatore MIDL disattiva tutte le informazioni sull'avviso.</span><span class="sxs-lookup"><span data-stu-id="3096a-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="3096a-117">In questo caso, l'opzione **/WX** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="3096a-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="3096a-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="3096a-118">Examples</span></span>

<span data-ttu-id="3096a-119">**MIDL/WX nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="3096a-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="3096a-120">**MIDL/W3/WX nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="3096a-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3096a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3096a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3096a-122">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="3096a-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3096a-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="3096a-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




