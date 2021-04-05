---
title: /syntax_check opzione
description: L' \_ opzione di controllo/Syntax indica che il compilatore controlla solo la sintassi e non genera file di output.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check switch MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718478"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="e8909-104">\_opzione di controllo/Syntax</span><span class="sxs-lookup"><span data-stu-id="e8909-104">/syntax\_check switch</span></span>

<span data-ttu-id="e8909-105">L'opzione di **\_ controllo/Syntax** indica che il compilatore controlla solo la sintassi e non genera file di output.</span><span class="sxs-lookup"><span data-stu-id="e8909-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="e8909-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="e8909-106">Switch Options</span></span>

<span data-ttu-id="e8909-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="e8909-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8909-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8909-108">Remarks</span></span>

<span data-ttu-id="e8909-109">Questa opzione esegue l'override di tutte le altre opzioni che specificano le informazioni sui file di output.</span><span class="sxs-lookup"><span data-stu-id="e8909-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="e8909-110">È anche possibile specificare la modalità di controllo della sintassi con l'opzione del compilatore MIDL [**/ZS**](-zs.md).</span><span class="sxs-lookup"><span data-stu-id="e8909-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e8909-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8909-111">Examples</span></span>

<span data-ttu-id="e8909-112">**MIDL/ZS nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="e8909-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="e8909-113">**MIDL/Syntax \_ controllare filename. idl**</span><span class="sxs-lookup"><span data-stu-id="e8909-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e8909-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8909-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8909-115">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="e8909-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e8909-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="e8909-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




