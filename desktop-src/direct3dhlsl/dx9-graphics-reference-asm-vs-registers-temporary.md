---
title: Registro temporaneo (riferimento HLSL VS)
description: Per mantenere i risultati intermedi, viene usato un registro temporaneo del vertex shader.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335692"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="9b7d4-103">Registro temporaneo (riferimento HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="9b7d4-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="9b7d4-104">Per mantenere i risultati intermedi, viene usato un registro temporaneo del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="9b7d4-105">Prima di utilizzare un registro temporaneo, è necessario inizializzarlo.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="9b7d4-106">Ogni registro temporaneo dispone di accesso in sola scrittura e di lettura tripla.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="9b7d4-107">Ciò significa che una singola istruzione shader può utilizzare fino a tre registri temporanei come input.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="9b7d4-108">Non è possibile usare i valori in un registro temporaneo che rimangono dalle chiamate precedenti del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="9b7d4-109">Un registro è costituito da proprietà che determinano il comportamento di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="9b7d4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b7d4-110">Property</span></span>        | <span data-ttu-id="9b7d4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b7d4-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7d4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9b7d4-112">Name</span></span>            | <span data-ttu-id="9b7d4-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="9b7d4-113">r\[n\].</span></span> <span data-ttu-id="9b7d4-114">n è un numero di registro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-114">n is an optional register number.</span></span> <span data-ttu-id="9b7d4-115">Il valore predefinito è 0 e è il valore utilizzato se non viene specificato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="9b7d4-116">Conteggio</span><span class="sxs-lookup"><span data-stu-id="9b7d4-116">Count</span></span>           | <span data-ttu-id="9b7d4-117">Un massimo di 12 registri.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="9b7d4-118">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="9b7d4-118">I/O permissions</span></span> | <span data-ttu-id="9b7d4-119">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-119">Read/write.</span></span> <span data-ttu-id="9b7d4-120">Questo registro può essere letto o scritto dall'API o dallo shader.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="9b7d4-121">Leggere le porte</span><span class="sxs-lookup"><span data-stu-id="9b7d4-121">Read ports</span></span>      | <span data-ttu-id="9b7d4-122">Il numero di volte in cui è possibile leggere un registro all'interno di una singola istruzione è 3.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="9b7d4-123">Un registro temporaneo è l'unico registro che può essere letto e scritto più di una volta in un'unica istruzione.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="9b7d4-124">Ogni registro temporaneo dispone di accesso in sola scrittura e di lettura tripla.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="9b7d4-125">Un'istruzione può pertanto avere fino a tre registri temporanei nel set di operandi di origine di input.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="9b7d4-126">Non è possibile usare alcun valore in un registro temporaneo che rimanga dalla chiamata precedente del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="9b7d4-127">I vertex shader che leggono un valore da un registro temporaneo prima di scrivervi non riusciranno a eseguire la chiamata all'API Direct3D per creare il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="9b7d4-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b7d4-128">Example</span></span>

<span data-ttu-id="9b7d4-129">Di seguito è riportato un esempio di utilizzo di un registro temporaneo:</span><span class="sxs-lookup"><span data-stu-id="9b7d4-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="9b7d4-130">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="9b7d4-130">Vertex shader versions</span></span> | <span data-ttu-id="9b7d4-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="9b7d4-131">1\_1</span></span> | <span data-ttu-id="9b7d4-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b7d4-132">2\_0</span></span> | <span data-ttu-id="9b7d4-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b7d4-133">2\_sw</span></span> | <span data-ttu-id="9b7d4-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-134">2\_x</span></span> | <span data-ttu-id="9b7d4-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9b7d4-135">3\_0</span></span> | <span data-ttu-id="9b7d4-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9b7d4-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="9b7d4-137">Registro temporaneo</span><span class="sxs-lookup"><span data-stu-id="9b7d4-137">Temporary Register</span></span>     | <span data-ttu-id="9b7d4-138">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-138">x</span></span>    | <span data-ttu-id="9b7d4-139">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-139">x</span></span>    | <span data-ttu-id="9b7d4-140">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-140">x</span></span>     | <span data-ttu-id="9b7d4-141">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-141">x</span></span>    | <span data-ttu-id="9b7d4-142">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-142">x</span></span>    | <span data-ttu-id="9b7d4-143">x</span><span class="sxs-lookup"><span data-stu-id="9b7d4-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="9b7d4-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b7d4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b7d4-145">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="9b7d4-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




