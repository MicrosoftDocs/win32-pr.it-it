---
title: RET-PS
description: Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione. Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976346"
---
# <a name="ret---ps"></a><span data-ttu-id="34bcc-104">RET-PS</span><span class="sxs-lookup"><span data-stu-id="34bcc-104">ret - ps</span></span>

<span data-ttu-id="34bcc-105">Accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="34bcc-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="34bcc-106">Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="34bcc-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bcc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34bcc-107">Syntax</span></span>



| <span data-ttu-id="34bcc-108">RET</span><span class="sxs-lookup"><span data-stu-id="34bcc-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="34bcc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="34bcc-109">Remarks</span></span>



| <span data-ttu-id="34bcc-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="34bcc-110">Pixel shader versions</span></span> | <span data-ttu-id="34bcc-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="34bcc-111">1\_1</span></span> | <span data-ttu-id="34bcc-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="34bcc-112">1\_2</span></span> | <span data-ttu-id="34bcc-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="34bcc-113">1\_3</span></span> | <span data-ttu-id="34bcc-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="34bcc-114">1\_4</span></span> | <span data-ttu-id="34bcc-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34bcc-115">2\_0</span></span> | <span data-ttu-id="34bcc-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="34bcc-116">2\_x</span></span> | <span data-ttu-id="34bcc-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34bcc-117">2\_sw</span></span> | <span data-ttu-id="34bcc-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="34bcc-118">3\_0</span></span> | <span data-ttu-id="34bcc-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="34bcc-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="34bcc-120">RET</span><span class="sxs-lookup"><span data-stu-id="34bcc-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="34bcc-121">x</span><span class="sxs-lookup"><span data-stu-id="34bcc-121">x</span></span>    | <span data-ttu-id="34bcc-122">x</span><span class="sxs-lookup"><span data-stu-id="34bcc-122">x</span></span>     | <span data-ttu-id="34bcc-123">x</span><span class="sxs-lookup"><span data-stu-id="34bcc-123">x</span></span>    | <span data-ttu-id="34bcc-124">x</span><span class="sxs-lookup"><span data-stu-id="34bcc-124">x</span></span>     |



 

<span data-ttu-id="34bcc-125">Questa istruzione accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="34bcc-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="34bcc-126">Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="34bcc-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="34bcc-127">L'istruzione RET usa uno slot di istruzioni vertex shader.</span><span class="sxs-lookup"><span data-stu-id="34bcc-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="34bcc-128">Se uno shader non contiene subroutine, l'utilizzo di RET alla fine del programma principale è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34bcc-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="34bcc-129">Non sono consentite più istruzioni return nel programma principale o in una subroutine, la prima istruzione return viene considerata come la fine del programma principale o della subroutine.</span><span class="sxs-lookup"><span data-stu-id="34bcc-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34bcc-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34bcc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34bcc-131">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="34bcc-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




