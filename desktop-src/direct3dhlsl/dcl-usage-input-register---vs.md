---
title: dcl_usage input (sm1, sm2, sm3 - vs asm)
description: Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input vertex shader.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129688"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="91065-103">dcl \_ usage input (sm1, sm2, sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="91065-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="91065-104">Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input vertex shader.</span><span class="sxs-lookup"><span data-stu-id="91065-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="91065-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91065-105">Syntax</span></span>

<span data-ttu-id="91065-106">dcl \_ usage usage index \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="91065-106">dcl\_usage\[usage\_index\] v\#</span></span>



 

<span data-ttu-id="91065-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="91065-107">Where:</span></span>

-   <span data-ttu-id="91065-108">dcl \_ usage identifica il modo in cui verranno usati i dati del registro.</span><span class="sxs-lookup"><span data-stu-id="91065-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="91065-109">Si tratta dello stesso valore dei membri di [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) senza il prefisso D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="91065-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="91065-110">usage \_ index è un indice integer facoltativo compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="91065-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="91065-111">Modifica i dati di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="91065-111">It modifies the usage data.</span></span> <span data-ttu-id="91065-112">L'indice corrisponde all'indice di utilizzo in una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="91065-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="91065-113">Vedere [Dichiarazione dei vertici (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration)</span><span class="sxs-lookup"><span data-stu-id="91065-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="91065-114">L'indice viene aggiunto al valore di utilizzo (utilizzo dcl \_ ) senza spazio.</span><span class="sxs-lookup"><span data-stu-id="91065-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="91065-115">Se non viene fornito, si presuppone che sia 0.</span><span class="sxs-lookup"><span data-stu-id="91065-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="91065-116">v \# è un registro di [input.](dx9-graphics-reference-asm-vs-registers-input.md)</span><span class="sxs-lookup"><span data-stu-id="91065-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91065-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="91065-117">Remarks</span></span>



| <span data-ttu-id="91065-118">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="91065-118">Vertex shader versions</span></span> | <span data-ttu-id="91065-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="91065-119">1\_1</span></span> | <span data-ttu-id="91065-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91065-120">2\_0</span></span> | <span data-ttu-id="91065-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="91065-121">2\_x</span></span> | <span data-ttu-id="91065-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="91065-122">2\_sw</span></span> | <span data-ttu-id="91065-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91065-123">3\_0</span></span> | <span data-ttu-id="91065-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="91065-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="91065-125">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="91065-125">dcl\_usage</span></span>             | <span data-ttu-id="91065-126">x</span><span class="sxs-lookup"><span data-stu-id="91065-126">x</span></span>    | <span data-ttu-id="91065-127">x</span><span class="sxs-lookup"><span data-stu-id="91065-127">x</span></span>    | <span data-ttu-id="91065-128">x</span><span class="sxs-lookup"><span data-stu-id="91065-128">x</span></span>    | <span data-ttu-id="91065-129">x</span><span class="sxs-lookup"><span data-stu-id="91065-129">x</span></span>     | <span data-ttu-id="91065-130">x</span><span class="sxs-lookup"><span data-stu-id="91065-130">x</span></span>    | <span data-ttu-id="91065-131">x</span><span class="sxs-lookup"><span data-stu-id="91065-131">x</span></span>     |



 

<span data-ttu-id="91065-132">Tutte le istruzioni dcl \_ usage devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="91065-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91065-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91065-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91065-134">Istruzioni per vertex shader</span><span class="sxs-lookup"><span data-stu-id="91065-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
