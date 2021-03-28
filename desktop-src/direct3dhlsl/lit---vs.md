---
title: Lit-vs
description: Fornisce un supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976394"
---
# <a name="lit---vs"></a><span data-ttu-id="9c508-103">Lit-vs</span><span class="sxs-lookup"><span data-stu-id="9c508-103">lit - vs</span></span>

<span data-ttu-id="9c508-104">Fornisce un supporto parziale per l'illuminazione calcolando i coefficienti di illuminazione da due prodotti punto e un esponente.</span><span class="sxs-lookup"><span data-stu-id="9c508-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c508-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c508-105">Syntax</span></span>



| <span data-ttu-id="9c508-106">Lit DST, src</span><span class="sxs-lookup"><span data-stu-id="9c508-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="9c508-107">dove</span><span class="sxs-lookup"><span data-stu-id="9c508-107">where</span></span>

-   <span data-ttu-id="9c508-108">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9c508-108">dst is the destination register.</span></span>
-   <span data-ttu-id="9c508-109">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="9c508-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c508-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c508-110">Remarks</span></span>



| <span data-ttu-id="9c508-111">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="9c508-111">Vertex shader versions</span></span> | <span data-ttu-id="9c508-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="9c508-112">1\_1</span></span> | <span data-ttu-id="9c508-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c508-113">2\_0</span></span> | <span data-ttu-id="9c508-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9c508-114">2\_x</span></span> | <span data-ttu-id="9c508-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c508-115">2\_sw</span></span> | <span data-ttu-id="9c508-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c508-116">3\_0</span></span> | <span data-ttu-id="9c508-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c508-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9c508-118">acceso</span><span class="sxs-lookup"><span data-stu-id="9c508-118">lit</span></span>                    | <span data-ttu-id="9c508-119">x</span><span class="sxs-lookup"><span data-stu-id="9c508-119">x</span></span>    | <span data-ttu-id="9c508-120">x</span><span class="sxs-lookup"><span data-stu-id="9c508-120">x</span></span>    | <span data-ttu-id="9c508-121">x</span><span class="sxs-lookup"><span data-stu-id="9c508-121">x</span></span>    | <span data-ttu-id="9c508-122">x</span><span class="sxs-lookup"><span data-stu-id="9c508-122">x</span></span>     | <span data-ttu-id="9c508-123">x</span><span class="sxs-lookup"><span data-stu-id="9c508-123">x</span></span>    | <span data-ttu-id="9c508-124">x</span><span class="sxs-lookup"><span data-stu-id="9c508-124">x</span></span>     |



 

<span data-ttu-id="9c508-125">Si presuppone che il vettore di origine contenga i valori mostrati nello pseudocodice seguente.</span><span class="sxs-lookup"><span data-stu-id="9c508-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="9c508-126">Nel frammento di codice seguente vengono illustrate le operazioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="9c508-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="9c508-127">L'aritmetica a precisione ridotta è accettabile per la valutazione del componente y di destinazione (dest. y).</span><span class="sxs-lookup"><span data-stu-id="9c508-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="9c508-128">Un'implementazione di deve supportare almeno otto bit di frazione nell'argomento di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="9c508-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="9c508-129">I prodotti dot vengono calcolati con vettori normalizzati e i limiti di clamp sono da-128 a 128.</span><span class="sxs-lookup"><span data-stu-id="9c508-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="9c508-130">È necessario che l'errore corrisponda a una combinazione di [LogP-vs](logp---vs.md) e [Exp-vs](exp---vs.md) oppure non più di circa un bit significativo per un componente colore a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="9c508-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c508-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c508-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c508-132">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="9c508-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




