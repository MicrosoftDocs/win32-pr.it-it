---
title: Opzione/ZS
description: L'opzione/ZS indica che il compilatore controlla solo la sintassi e non genera file di output.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /ZS switch MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718163"
---
# <a name="zs-switch"></a><span data-ttu-id="a083c-104">Opzione/ZS</span><span class="sxs-lookup"><span data-stu-id="a083c-104">/Zs switch</span></span>

<span data-ttu-id="a083c-105">L'opzione **/ZS** indica che il compilatore controlla solo la sintassi e non genera file di output.</span><span class="sxs-lookup"><span data-stu-id="a083c-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="a083c-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="a083c-106">Switch Options</span></span>

<span data-ttu-id="a083c-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a083c-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a083c-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a083c-108">Remarks</span></span>

<span data-ttu-id="a083c-109">Questa opzione esegue l'override di tutte le altre opzioni che specificano le informazioni sui file di output.</span><span class="sxs-lookup"><span data-stu-id="a083c-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="a083c-110">È anche possibile specificare la modalità di controllo della sintassi con il [**\_ controllo/Syntax**](-syntax-check.md)dell'opzione del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="a083c-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a083c-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="a083c-111">Examples</span></span>

<span data-ttu-id="a083c-112">**MIDL/ZS nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="a083c-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="a083c-113">**MIDL/Syntax \_ controllare filename. idl**</span><span class="sxs-lookup"><span data-stu-id="a083c-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a083c-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a083c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a083c-115">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="a083c-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a083c-116">**\_controllo/Syntax**</span><span class="sxs-lookup"><span data-stu-id="a083c-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




