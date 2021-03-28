---
title: texreg2rgb-PS
description: Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati degli indirizzi di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione. Il risultato viene archiviato nel registro di destinazione.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516495"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="1f374-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="1f374-104">texreg2rgb - ps</span></span>

<span data-ttu-id="1f374-105">Interpreta i componenti di colore rosso, verde e blu (RGB) del registro di origine come dati degli indirizzi di trama per campionare la trama in corrispondenza della fase corrispondente al numero di registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f374-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="1f374-106">Il risultato viene archiviato nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f374-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f374-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f374-107">Syntax</span></span>



| <span data-ttu-id="1f374-108">texreg2rgb DST, src</span><span class="sxs-lookup"><span data-stu-id="1f374-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="1f374-109">dove</span><span class="sxs-lookup"><span data-stu-id="1f374-109">where</span></span>

-   <span data-ttu-id="1f374-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f374-110">dst is the destination register.</span></span>
-   <span data-ttu-id="1f374-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="1f374-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f374-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f374-112">Remarks</span></span>



| <span data-ttu-id="1f374-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1f374-113">Pixel shader versions</span></span> | <span data-ttu-id="1f374-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="1f374-114">1\_1</span></span> | <span data-ttu-id="1f374-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="1f374-115">1\_2</span></span> | <span data-ttu-id="1f374-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1f374-116">1\_3</span></span> | <span data-ttu-id="1f374-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="1f374-117">1\_4</span></span> | <span data-ttu-id="1f374-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f374-118">2\_0</span></span> | <span data-ttu-id="1f374-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1f374-119">2\_x</span></span> | <span data-ttu-id="1f374-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1f374-120">2\_sw</span></span> | <span data-ttu-id="1f374-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f374-121">3\_0</span></span> | <span data-ttu-id="1f374-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1f374-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1f374-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="1f374-123">texreg2rgb</span></span>            |      | <span data-ttu-id="1f374-124">x</span><span class="sxs-lookup"><span data-stu-id="1f374-124">x</span></span>    | <span data-ttu-id="1f374-125">x</span><span class="sxs-lookup"><span data-stu-id="1f374-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="1f374-126">Questa istruzione è utile per le operazioni di rimapping dello spazio colore.</span><span class="sxs-lookup"><span data-stu-id="1f374-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="1f374-127">Supporta le coordinate bidimensionali (2D) e tridimensionali (3D).</span><span class="sxs-lookup"><span data-stu-id="1f374-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="1f374-128">Può essere usato come [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md) per modificare il mapping dei dati 2D.</span><span class="sxs-lookup"><span data-stu-id="1f374-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="1f374-129">Tuttavia, questa istruzione supporta anche i dati 3D, in modo che possano essere utilizzati con le mappe del cubo e le trame del volume 3D.</span><span class="sxs-lookup"><span data-stu-id="1f374-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="1f374-130">Di seguito è riportato un esempio della sequenza che segue l'istruzione.</span><span class="sxs-lookup"><span data-stu-id="1f374-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="1f374-131">Di seguito sono riportati altri dettagli sul modo in cui viene eseguito il mapping.</span><span class="sxs-lookup"><span data-stu-id="1f374-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="1f374-132">La prima istruzione carica il colore della trama (RGBA) nel registro TN</span><span class="sxs-lookup"><span data-stu-id="1f374-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="1f374-133">Tex TN</span><span class="sxs-lookup"><span data-stu-id="1f374-133">tex tn</span></span>  
<span data-ttu-id="1f374-134">La seconda istruzione esegue il mapping del colore</span><span class="sxs-lookup"><span data-stu-id="1f374-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="1f374-135">t (m)<sub>RGBA</sub> = TextureSample (fase m)<sub>RGBA</sub> utilizzo di t (n)<sub>RGB</sub> come coordinate</span><span class="sxs-lookup"><span data-stu-id="1f374-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="1f374-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f374-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f374-137">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="1f374-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




