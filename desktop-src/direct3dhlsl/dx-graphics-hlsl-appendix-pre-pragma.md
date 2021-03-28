---
title: " pragma (direttiva)"
description: Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo la compatibilità complessiva con i linguaggi C e C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- pragma directive HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045738"
---
# <a name="pragma-directive"></a><span data-ttu-id="a270a-104">\#pragma (direttiva)</span><span class="sxs-lookup"><span data-stu-id="a270a-104">\#pragma Directive</span></span>

<span data-ttu-id="a270a-105">Direttiva per il preprocessore che fornisce funzionalità specifiche del computer o del sistema operativo mantenendo la compatibilità complessiva con i linguaggi C e C++.</span><span class="sxs-lookup"><span data-stu-id="a270a-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="a270a-106">\#pragma *-stringa di token*</span><span class="sxs-lookup"><span data-stu-id="a270a-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a270a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a270a-107">Parameters</span></span>



| <span data-ttu-id="a270a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a270a-108">Item</span></span>                                                                                    | <span data-ttu-id="a270a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a270a-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a270a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*</span><span class="sxs-lookup"><span data-stu-id="a270a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="a270a-111">Serie di caratteri che fornisce un'istruzione e argomenti specifici del compilatore.</span><span class="sxs-lookup"><span data-stu-id="a270a-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="a270a-112">Questo parametro è soggetto all'espansione della macro.</span><span class="sxs-lookup"><span data-stu-id="a270a-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a270a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a270a-113">Remarks</span></span>

<span data-ttu-id="a270a-114">Se il compilatore trova un pragma che non riconosce, genera un avviso, ma la compilazione continua.</span><span class="sxs-lookup"><span data-stu-id="a270a-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="a270a-115">Il compilatore HLSL riconosce i seguenti pragma:</span><span class="sxs-lookup"><span data-stu-id="a270a-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="a270a-116">def</span><span class="sxs-lookup"><span data-stu-id="a270a-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="a270a-117">message</span><span class="sxs-lookup"><span data-stu-id="a270a-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="a270a-118">matrice di pacchetti \_</span><span class="sxs-lookup"><span data-stu-id="a270a-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="a270a-119">warning</span><span class="sxs-lookup"><span data-stu-id="a270a-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="a270a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a270a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a270a-121">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a270a-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





