---
title: Posizione registro
description: Questo registro di output del vertex shader contiene dati di posizione per vertice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711086"
---
# <a name="position-register"></a><span data-ttu-id="60b5e-103">Posizione registro</span><span class="sxs-lookup"><span data-stu-id="60b5e-103">Position Register</span></span>

<span data-ttu-id="60b5e-104">Questo registro di output del vertex shader contiene dati di posizione per vertice.</span><span class="sxs-lookup"><span data-stu-id="60b5e-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="60b5e-105">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="60b5e-105">Vertex shader versions</span></span> | <span data-ttu-id="60b5e-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="60b5e-106">1\_1</span></span> | <span data-ttu-id="60b5e-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60b5e-107">2\_0</span></span> | <span data-ttu-id="60b5e-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="60b5e-108">2\_sw</span></span> | <span data-ttu-id="60b5e-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="60b5e-109">2\_x</span></span> | <span data-ttu-id="60b5e-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60b5e-110">3\_0</span></span> | <span data-ttu-id="60b5e-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="60b5e-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="60b5e-112">Posizione registro</span><span class="sxs-lookup"><span data-stu-id="60b5e-112">Position Register</span></span>      | <span data-ttu-id="60b5e-113">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-113">x</span></span>    | <span data-ttu-id="60b5e-114">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-114">x</span></span>    | <span data-ttu-id="60b5e-115">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-115">x</span></span>     | <span data-ttu-id="60b5e-116">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-116">x</span></span>    | <span data-ttu-id="60b5e-117">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-117">x</span></span>    | <span data-ttu-id="60b5e-118">x</span><span class="sxs-lookup"><span data-stu-id="60b5e-118">x</span></span>     |



 

<span data-ttu-id="60b5e-119">Un registro è costituito da proprietà che determinano il comportamento di ogni registro.</span><span class="sxs-lookup"><span data-stu-id="60b5e-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="60b5e-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="60b5e-120">Property</span></span>        | <span data-ttu-id="60b5e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60b5e-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="60b5e-122">Nome</span><span class="sxs-lookup"><span data-stu-id="60b5e-122">Name</span></span>            | <span data-ttu-id="60b5e-123">oPos</span><span class="sxs-lookup"><span data-stu-id="60b5e-123">oPos</span></span>        |
| <span data-ttu-id="60b5e-124">Conteggio</span><span class="sxs-lookup"><span data-stu-id="60b5e-124">Count</span></span>           | <span data-ttu-id="60b5e-125">1 vettore</span><span class="sxs-lookup"><span data-stu-id="60b5e-125">1 vector</span></span>    |
| <span data-ttu-id="60b5e-126">Autorizzazioni di I/O</span><span class="sxs-lookup"><span data-stu-id="60b5e-126">I/O permissions</span></span> | <span data-ttu-id="60b5e-127">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="60b5e-127">Write-only.</span></span> |



 

<span data-ttu-id="60b5e-128">Il valore è la posizione nello spazio di ritaglio omogeneo.</span><span class="sxs-lookup"><span data-stu-id="60b5e-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="60b5e-129">Questo valore deve essere scritto dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="60b5e-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="60b5e-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="60b5e-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="60b5e-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60b5e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60b5e-132">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="60b5e-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




