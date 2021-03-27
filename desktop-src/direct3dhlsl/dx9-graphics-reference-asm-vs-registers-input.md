---
title: Registro di input
description: Registro di input
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955614"
---
# <a name="input-register"></a><span data-ttu-id="96654-103">Registro di input</span><span class="sxs-lookup"><span data-stu-id="96654-103">Input Register</span></span>

<span data-ttu-id="96654-104">Registro di input vertex shader.</span><span class="sxs-lookup"><span data-stu-id="96654-104">Vertex shader input register.</span></span>

<span data-ttu-id="96654-105">I dati di ogni vertice (usando uno o più flussi di vertici di input) vengono caricati nei registri di input dei vertici prima dell'esecuzione del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="96654-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="96654-106">I registri di input sono costituiti da vettori a virgola mobile a 16 4 componenti, designati come V0 tramite versione 15.</span><span class="sxs-lookup"><span data-stu-id="96654-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="96654-107">Questi registri sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="96654-107">These registers are read-only.</span></span> <span data-ttu-id="96654-108">Un registro di input è associato ai dati dei vertici tramite una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="96654-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="96654-109">Le proprietà Register seguenti controllano il comportamento di ogni registro:</span><span class="sxs-lookup"><span data-stu-id="96654-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="96654-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96654-110">Property</span></span>        | <span data-ttu-id="96654-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96654-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96654-112">Nome</span><span class="sxs-lookup"><span data-stu-id="96654-112">Name</span></span>            | <span data-ttu-id="96654-113">v \[ n \] -n è un numero di registro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="96654-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="96654-114">0 è il valore predefinito usato, se viene omesso.</span><span class="sxs-lookup"><span data-stu-id="96654-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="96654-115">Conteggio</span><span class="sxs-lookup"><span data-stu-id="96654-115">Count</span></span>           | <span data-ttu-id="96654-116">Un massimo di 16 registri, V0-versione 15.</span><span class="sxs-lookup"><span data-stu-id="96654-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="96654-117">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="96654-117">I/O permissions</span></span> | <span data-ttu-id="96654-118">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="96654-118">Read-only.</span></span> <span data-ttu-id="96654-119">Questo registro non può essere scritto dall'API o nello shader.</span><span class="sxs-lookup"><span data-stu-id="96654-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="96654-120">Leggere le porte</span><span class="sxs-lookup"><span data-stu-id="96654-120">Read ports</span></span>      | <span data-ttu-id="96654-121">1. indica il numero di volte in cui è possibile leggere un registro all'interno di un'unica istruzione.</span><span class="sxs-lookup"><span data-stu-id="96654-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="96654-122">Vedere qui di seguito.</span><span class="sxs-lookup"><span data-stu-id="96654-122">See below.</span></span> |



 

<span data-ttu-id="96654-123">Ogni singola istruzione può accedere a un solo registro di input del vertice.</span><span class="sxs-lookup"><span data-stu-id="96654-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="96654-124">Tuttavia, ogni origine nell'istruzione può swizzle in modo indipendente e negare il vettore mentre viene letto.</span><span class="sxs-lookup"><span data-stu-id="96654-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="96654-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="96654-125">Example</span></span>

<span data-ttu-id="96654-126">Di seguito è riportato un esempio di utilizzo di una dichiarazione vertex per associare i dati della posizione del vertice 2D al registro V0.</span><span class="sxs-lookup"><span data-stu-id="96654-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="96654-127">La dichiarazione di vertice appartiene all'applicazione:</span><span class="sxs-lookup"><span data-stu-id="96654-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="96654-128">Di seguito è illustrata la dichiarazione vertex shader corrispondente:</span><span class="sxs-lookup"><span data-stu-id="96654-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="96654-129">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="96654-129">Vertex shader versions</span></span> | <span data-ttu-id="96654-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="96654-130">1\_1</span></span> | <span data-ttu-id="96654-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96654-131">2\_0</span></span> | <span data-ttu-id="96654-132">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96654-132">2\_sw</span></span> | <span data-ttu-id="96654-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96654-133">2\_x</span></span> | <span data-ttu-id="96654-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96654-134">3\_0</span></span> | <span data-ttu-id="96654-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96654-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="96654-136">Posizione registro</span><span class="sxs-lookup"><span data-stu-id="96654-136">Position Register</span></span>      | <span data-ttu-id="96654-137">x</span><span class="sxs-lookup"><span data-stu-id="96654-137">x</span></span>    | <span data-ttu-id="96654-138">x</span><span class="sxs-lookup"><span data-stu-id="96654-138">x</span></span>    | <span data-ttu-id="96654-139">x</span><span class="sxs-lookup"><span data-stu-id="96654-139">x</span></span>     | <span data-ttu-id="96654-140">x</span><span class="sxs-lookup"><span data-stu-id="96654-140">x</span></span>    | <span data-ttu-id="96654-141">x</span><span class="sxs-lookup"><span data-stu-id="96654-141">x</span></span>    | <span data-ttu-id="96654-142">x</span><span class="sxs-lookup"><span data-stu-id="96654-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="96654-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96654-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96654-144">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="96654-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




