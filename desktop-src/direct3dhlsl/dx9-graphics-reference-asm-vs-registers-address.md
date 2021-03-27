---
title: Registro indirizzi
description: Il registro a0 è un registro degli indirizzi.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856582"
---
# <a name="address-register"></a><span data-ttu-id="5b182-103">Registro indirizzi</span><span class="sxs-lookup"><span data-stu-id="5b182-103">Address Register</span></span>

<span data-ttu-id="5b182-104">Il registro a0 è un registro degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="5b182-104">The a0 register is an address register.</span></span> <span data-ttu-id="5b182-105">Un singolo registro è disponibile nella versione di Visual Studio \_ 1 \_ .</span><span class="sxs-lookup"><span data-stu-id="5b182-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="5b182-106">Il registro degli indirizzi, designato come a0. x in Visual Studio 1 \_ \_ , può essere usato come offset intero con segno per l'indirizzamento relativo nel file di registro delle costanti.</span><span class="sxs-lookup"><span data-stu-id="5b182-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="5b182-107">Per le versioni vs \_ 2 \_ 0 e successive, tutti i quattro componenti (. x,. y,. z,. w) sono disponibili per l'indirizzamento relativo.</span><span class="sxs-lookup"><span data-stu-id="5b182-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="5b182-108">Il registro degli indirizzi non può essere letto da un vertex shader. può essere usato solo per l'indirizzamento relativo di un registro costante.</span><span class="sxs-lookup"><span data-stu-id="5b182-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="5b182-109">La lettura di valori al di fuori dell'intervallo valido restituirà (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="5b182-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="5b182-110">Il registro degli indirizzi può essere solo una destinazione per l'istruzione [MOV-vs](mov---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="5b182-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="5b182-111">Se un numero a virgola mobile viene spostato in un registro Integer, viene eseguita una conversione round-to-most più vicina.</span><span class="sxs-lookup"><span data-stu-id="5b182-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="5b182-112">Tutti gli shader devono inizializzare il registro degli indirizzi prima di usarlo.</span><span class="sxs-lookup"><span data-stu-id="5b182-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="5b182-113">Per la versione vs \_ 2 \_ 0 e successive, l'istruzione [mova-vs](mova---vs.md) può spostare un valore a virgola mobile in un registro di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="5b182-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="5b182-114">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="5b182-114">Vertex shader versions</span></span> | <span data-ttu-id="5b182-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b182-115">1\_1</span></span> | <span data-ttu-id="5b182-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b182-116">2\_0</span></span> | <span data-ttu-id="5b182-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b182-117">2\_sw</span></span> | <span data-ttu-id="5b182-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b182-118">2\_x</span></span> | <span data-ttu-id="5b182-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b182-119">3\_0</span></span> | <span data-ttu-id="5b182-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b182-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="5b182-121">Registro indirizzi</span><span class="sxs-lookup"><span data-stu-id="5b182-121">Address Register</span></span>       | <span data-ttu-id="5b182-122">x</span><span class="sxs-lookup"><span data-stu-id="5b182-122">x</span></span>    | <span data-ttu-id="5b182-123">x</span><span class="sxs-lookup"><span data-stu-id="5b182-123">x</span></span>    | <span data-ttu-id="5b182-124">x</span><span class="sxs-lookup"><span data-stu-id="5b182-124">x</span></span>     | <span data-ttu-id="5b182-125">x</span><span class="sxs-lookup"><span data-stu-id="5b182-125">x</span></span>    | <span data-ttu-id="5b182-126">x</span><span class="sxs-lookup"><span data-stu-id="5b182-126">x</span></span>    | <span data-ttu-id="5b182-127">x</span><span class="sxs-lookup"><span data-stu-id="5b182-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5b182-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b182-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b182-129">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="5b182-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




