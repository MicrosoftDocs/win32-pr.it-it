---
title: RET-vs
description: Restituisce da una subroutine o da una funzione Main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335495"
---
# <a name="ret---vs"></a><span data-ttu-id="86436-103">RET-vs</span><span class="sxs-lookup"><span data-stu-id="86436-103">ret - vs</span></span>

<span data-ttu-id="86436-104">Restituisce da una subroutine o da una funzione Main.</span><span class="sxs-lookup"><span data-stu-id="86436-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="86436-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86436-105">Syntax</span></span>



| <span data-ttu-id="86436-106">RET</span><span class="sxs-lookup"><span data-stu-id="86436-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="86436-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="86436-107">Remarks</span></span>



| <span data-ttu-id="86436-108">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="86436-108">Vertex shader versions</span></span> | <span data-ttu-id="86436-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="86436-109">1\_1</span></span> | <span data-ttu-id="86436-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86436-110">2\_0</span></span> | <span data-ttu-id="86436-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="86436-111">2\_x</span></span> | <span data-ttu-id="86436-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86436-112">2\_sw</span></span> | <span data-ttu-id="86436-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86436-113">3\_0</span></span> | <span data-ttu-id="86436-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="86436-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="86436-115">RET</span><span class="sxs-lookup"><span data-stu-id="86436-115">ret</span></span>                    |      | <span data-ttu-id="86436-116">x</span><span class="sxs-lookup"><span data-stu-id="86436-116">x</span></span>    | <span data-ttu-id="86436-117">x</span><span class="sxs-lookup"><span data-stu-id="86436-117">x</span></span>    | <span data-ttu-id="86436-118">x</span><span class="sxs-lookup"><span data-stu-id="86436-118">x</span></span>     | <span data-ttu-id="86436-119">x</span><span class="sxs-lookup"><span data-stu-id="86436-119">x</span></span>    | <span data-ttu-id="86436-120">x</span><span class="sxs-lookup"><span data-stu-id="86436-120">x</span></span>     |



 

<span data-ttu-id="86436-121">Questa istruzione accetta l'indirizzo di un'istruzione dallo stack di indirizzi restituiti e continua l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86436-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="86436-122">Nel caso della funzione Main, questa istruzione arresta l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="86436-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="86436-123">L'istruzione RET usa uno slot di istruzioni vertex shader.</span><span class="sxs-lookup"><span data-stu-id="86436-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="86436-124">Se uno shader non contiene subroutine, l'utilizzo di RET alla fine del programma principale è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="86436-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="86436-125">Non sono consentite più istruzioni return nel programma principale o in una subroutine, la prima istruzione return viene considerata come la fine del programma principale o della subroutine.</span><span class="sxs-lookup"><span data-stu-id="86436-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86436-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86436-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86436-127">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="86436-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




