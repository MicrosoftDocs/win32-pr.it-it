---
title: input dcl_usage (SM1, SM2, SM3-vs ASM)
description: Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input del vertex shader.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473534"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="70cb6-103">\_input utilizzo DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="70cb6-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="70cb6-104">Dichiarare l'associazione tra l'utilizzo di un elemento vertice e un indice di utilizzo per un registro di input del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="70cb6-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70cb6-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="70cb6-106">\_ \[ Indice utilizzo utilizzo \_ DCL \] v\#</span><span class="sxs-lookup"><span data-stu-id="70cb6-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="70cb6-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="70cb6-107">Where:</span></span>

-   <span data-ttu-id="70cb6-108">\_l'utilizzo di DCL identifica il modo in cui verranno usati i dati del registro.</span><span class="sxs-lookup"><span data-stu-id="70cb6-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="70cb6-109">Si tratta dello stesso valore dei membri di [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) senza il prefisso D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="70cb6-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="70cb6-110">Usage \_ index è un indice integer facoltativo compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="70cb6-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="70cb6-111">Modifica i dati di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="70cb6-111">It modifies the usage data.</span></span> <span data-ttu-id="70cb6-112">L'indice corrisponde all'indice di utilizzo in una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="70cb6-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="70cb6-113">Vedere [dichiarazione vertici (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="70cb6-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="70cb6-114">L'indice viene aggiunto al valore di utilizzo ( \_ utilizzo di DCL) senza spazio.</span><span class="sxs-lookup"><span data-stu-id="70cb6-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="70cb6-115">Se non viene specificato, si presuppone che sia 0.</span><span class="sxs-lookup"><span data-stu-id="70cb6-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="70cb6-116">v \# è un [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="70cb6-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70cb6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="70cb6-117">Remarks</span></span>



| <span data-ttu-id="70cb6-118">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="70cb6-118">Vertex shader versions</span></span> | <span data-ttu-id="70cb6-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="70cb6-119">1\_1</span></span> | <span data-ttu-id="70cb6-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70cb6-120">2\_0</span></span> | <span data-ttu-id="70cb6-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="70cb6-121">2\_x</span></span> | <span data-ttu-id="70cb6-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70cb6-122">2\_sw</span></span> | <span data-ttu-id="70cb6-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70cb6-123">3\_0</span></span> | <span data-ttu-id="70cb6-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="70cb6-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="70cb6-125">utilizzo di DCL \_</span><span class="sxs-lookup"><span data-stu-id="70cb6-125">dcl\_usage</span></span>             | <span data-ttu-id="70cb6-126">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-126">x</span></span>    | <span data-ttu-id="70cb6-127">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-127">x</span></span>    | <span data-ttu-id="70cb6-128">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-128">x</span></span>    | <span data-ttu-id="70cb6-129">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-129">x</span></span>     | <span data-ttu-id="70cb6-130">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-130">x</span></span>    | <span data-ttu-id="70cb6-131">x</span><span class="sxs-lookup"><span data-stu-id="70cb6-131">x</span></span>     |



 

<span data-ttu-id="70cb6-132">Tutte le \_ istruzioni di utilizzo di DCL devono essere visualizzate prima della prima istruzione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="70cb6-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70cb6-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70cb6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70cb6-134">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="70cb6-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 