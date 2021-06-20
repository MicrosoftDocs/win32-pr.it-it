---
title: Registro contatori cicli (informazioni di riferimento su HLSL VS)
description: Informazioni sul registro dei contatori del ciclo per i vertex shader. L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405774"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="115cd-104">Registro contatori cicli (informazioni di riferimento su HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="115cd-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="115cd-105">L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL).</span><span class="sxs-lookup"><span data-stu-id="115cd-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="115cd-106">Viene incrementato automaticamente in ogni esecuzione del [ciclo , rispetto a](loop---vs.md)... [endloop - vs](endloop---vs.md) block.</span><span class="sxs-lookup"><span data-stu-id="115cd-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="115cd-107">Può quindi essere usato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per usarlo all'esterno del ciclo.</span><span class="sxs-lookup"><span data-stu-id="115cd-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="115cd-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="115cd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="115cd-109">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="115cd-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




