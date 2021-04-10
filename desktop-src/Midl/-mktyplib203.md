---
title: opzione/mktyplib203
description: L'opzione/mktyplib203 impone al compilatore MIDL di analizzare il file di input.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 switch MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857550"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="8770f-104">opzione/mktyplib203</span><span class="sxs-lookup"><span data-stu-id="8770f-104">/mktyplib203 switch</span></span>

<span data-ttu-id="8770f-105">L'opzione **/mktyplib203** impone al compilatore MIDL di analizzare il file di input.</span><span class="sxs-lookup"><span data-stu-id="8770f-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="8770f-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="8770f-106">Switch Options</span></span>

<span data-ttu-id="8770f-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="8770f-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8770f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8770f-108">Remarks</span></span>

<span data-ttu-id="8770f-109">Per usare l'opzione **/mktyplib203** , è necessario che il file di input segua esattamente la sintassi di FAD. non è quindi possibile inserire istruzioni all'esterno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="8770f-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="8770f-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="8770f-110">Examples</span></span>

<span data-ttu-id="8770f-111">**MIDL/mktyplib203 myoldodl. FAD**</span><span class="sxs-lookup"><span data-stu-id="8770f-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="8770f-112">**MIDL/mktyplib203 oldhabit. idl**</span><span class="sxs-lookup"><span data-stu-id="8770f-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="8770f-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8770f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8770f-114">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="8770f-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8770f-115">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="8770f-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




