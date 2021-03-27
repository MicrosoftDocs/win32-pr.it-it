---
title: Registro colori di input
description: Registro di input pixel shader che contiene il colore del vertice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396951"
---
# <a name="input-color-register"></a><span data-ttu-id="31151-103">Registro colori di input</span><span class="sxs-lookup"><span data-stu-id="31151-103">Input Color Register</span></span>

<span data-ttu-id="31151-104">Registro di input pixel shader che contiene il colore del vertice.</span><span class="sxs-lookup"><span data-stu-id="31151-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="31151-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31151-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="31151-106">dove:</span><span class="sxs-lookup"><span data-stu-id="31151-106">where:</span></span>

-   <span data-ttu-id="31151-107">[DCL-(SM2, SM3-PS ASM)](dcl---ps.md) è un'istruzione di dichiarazione Register.</span><span class="sxs-lookup"><span data-stu-id="31151-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="31151-108">v è un registro di input ed \# è il numero di registro.</span><span class="sxs-lookup"><span data-stu-id="31151-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="31151-109">Il numero di registri consentito è determinato dalla versione dello shader.</span><span class="sxs-lookup"><span data-stu-id="31151-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="31151-110">writeMask determina quali componenti (fino a quattro) vengono scritti.</span><span class="sxs-lookup"><span data-stu-id="31151-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="31151-111">I componenti validi sono: (x, y, z, w) o (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="31151-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="31151-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="31151-112">Remarks</span></span>

<span data-ttu-id="31151-113">I registri colori sono registri di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="31151-113">Color registers are read-only registers.</span></span> <span data-ttu-id="31151-114">Ogni registro contiene valori RGBA a quattro componenti iterati dai vertici di input.</span><span class="sxs-lookup"><span data-stu-id="31151-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="31151-115">Hanno una precisione inferiore rispetto alla maggior parte dei registri, con una garanzia di 8 bit di dati non firmati nell'intervallo (0, + 1).</span><span class="sxs-lookup"><span data-stu-id="31151-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="31151-116">Non è possibile usare più di uno in un'unica istruzione.</span><span class="sxs-lookup"><span data-stu-id="31151-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31151-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31151-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31151-118">Registri</span><span class="sxs-lookup"><span data-stu-id="31151-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="31151-119">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="31151-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="31151-120">\_registri PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31151-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="31151-121">\_registri PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31151-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="31151-122">\_registri PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31151-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




