---
title: opzione/notlb
description: L'opzione/notlb impedisce al compilatore MIDL di generare un file della libreria dei tipi (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb switch MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471966"
---
# <a name="notlb-switch"></a><span data-ttu-id="d09fc-104">opzione/notlb</span><span class="sxs-lookup"><span data-stu-id="d09fc-104">/notlb switch</span></span>

<span data-ttu-id="d09fc-105">L'opzione **/notlb** impedisce al compilatore MIDL di generare un file della libreria dei tipi (tlb).</span><span class="sxs-lookup"><span data-stu-id="d09fc-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="d09fc-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="d09fc-106">Switch Options</span></span>

<span data-ttu-id="d09fc-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d09fc-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09fc-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d09fc-108">Remarks</span></span>

<span data-ttu-id="d09fc-109">Per impostazione predefinita, il compilatore MIDL genererà un file TLB ogni volta che viene rilevata un'istruzione di [**libreria**](library.md) .</span><span class="sxs-lookup"><span data-stu-id="d09fc-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="d09fc-110">Questa opzione sostituisce il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="d09fc-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="d09fc-111">Quando si specifica l'opzione **/notlb** , tutti gli altri Stub, intestazioni e così via vengono generati come di consueto.</span><span class="sxs-lookup"><span data-stu-id="d09fc-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="d09fc-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d09fc-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09fc-113">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="d09fc-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




