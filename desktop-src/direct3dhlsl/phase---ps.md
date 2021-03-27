---
title: fase-PS
description: L'istruzione Phase contrassegna la transizione tra la fase 1 e la fase 2. Se non è presente alcuna istruzione della fase, l'intero shader viene eseguito come se fosse uno shader della fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046113"
---
# <a name="phase---ps"></a><span data-ttu-id="138db-104">fase-PS</span><span class="sxs-lookup"><span data-stu-id="138db-104">phase - ps</span></span>

<span data-ttu-id="138db-105">L'istruzione Phase contrassegna la transizione tra la fase 1 e la fase 2.</span><span class="sxs-lookup"><span data-stu-id="138db-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="138db-106">Se non è presente alcuna istruzione della fase, l'intero shader viene eseguito come se fosse uno shader della fase 2.</span><span class="sxs-lookup"><span data-stu-id="138db-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="138db-107">Questa istruzione si applica solo alla versione 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="138db-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="138db-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="138db-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="138db-109">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="138db-109">Remarks</span></span>



| <span data-ttu-id="138db-110">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="138db-110">Pixel shader versions</span></span> | <span data-ttu-id="138db-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="138db-111">1\_1</span></span> | <span data-ttu-id="138db-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="138db-112">1\_2</span></span> | <span data-ttu-id="138db-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="138db-113">1\_3</span></span> | <span data-ttu-id="138db-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="138db-114">1\_4</span></span> | <span data-ttu-id="138db-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="138db-115">2\_0</span></span> | <span data-ttu-id="138db-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="138db-116">2\_x</span></span> | <span data-ttu-id="138db-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="138db-117">2\_sw</span></span> | <span data-ttu-id="138db-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="138db-118">3\_0</span></span> | <span data-ttu-id="138db-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="138db-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="138db-120">fase</span><span class="sxs-lookup"><span data-stu-id="138db-120">phase</span></span>                 |      |      |      | <span data-ttu-id="138db-121">x</span><span class="sxs-lookup"><span data-stu-id="138db-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="138db-122">Le istruzioni dello shader che si verificano prima dell'istruzione Phase sono le istruzioni della fase 1.</span><span class="sxs-lookup"><span data-stu-id="138db-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="138db-123">Tutte le altre istruzioni sono le istruzioni della fase 2.</span><span class="sxs-lookup"><span data-stu-id="138db-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="138db-124">Con due fasi per le istruzioni, viene aumentato il numero massimo di istruzioni per shader.</span><span class="sxs-lookup"><span data-stu-id="138db-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="138db-125">Lo sfortunato effetto collaterale della transizione della fase è che il componente alfa dei [registri temporanei](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) non viene mantenuto durante la transizione.</span><span class="sxs-lookup"><span data-stu-id="138db-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="138db-126">In altre parole, è necessario reinizializzare il componente alfa dopo l'istruzione Phase.</span><span class="sxs-lookup"><span data-stu-id="138db-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="138db-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="138db-127">Example</span></span>

<span data-ttu-id="138db-128">Questo esempio illustra come raggruppare le istruzioni come fase 1 o le istruzioni della fase 2 in uno shader.</span><span class="sxs-lookup"><span data-stu-id="138db-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="138db-129">L'istruzione Phase viene comunemente chiamata marcatore fase perché contrassegna la transizione tra le istruzioni Phase 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="138db-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="138db-130">In una versione 1 \_ 4 pixel shader, se il marcatore di fase non è presente, lo shader viene eseguito come se fosse in esecuzione nella fase 2.</span><span class="sxs-lookup"><span data-stu-id="138db-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="138db-131">Questo aspetto è importante perché esistono differenze tra le istruzioni Phase 1 e 2 e la disponibilità del registro.</span><span class="sxs-lookup"><span data-stu-id="138db-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="138db-132">Le differenze sono indicate nella sezione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="138db-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="138db-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="138db-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="138db-134">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="138db-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




