---
title: Registro del contatore di cicli (riferimento HLSL VS)
description: L'unico registro in questa banca è il registro del contatore di cicli corrente (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104398325"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="ea5f5-103">Registro del contatore di cicli (riferimento HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="ea5f5-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="ea5f5-104">L'unico registro in questa banca è il registro del contatore di cicli corrente (aL).</span><span class="sxs-lookup"><span data-stu-id="ea5f5-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="ea5f5-105">Viene incrementato automaticamente in ogni esecuzione del [ciclo-vs](loop---vs.md)... blocco [EndLoop-vs](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="ea5f5-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="ea5f5-106">Pertanto, può essere utilizzato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per utilizzarlo all'esterno del ciclo.</span><span class="sxs-lookup"><span data-stu-id="ea5f5-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea5f5-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ea5f5-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea5f5-108">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="ea5f5-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




