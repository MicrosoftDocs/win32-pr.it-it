---
title: opzione/SAL
description: L'opzione/Sal indica a MIDL di generare le annotazioni SAL nei file stub generati.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /Sal switch MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299091"
---
# <a name="sal-switch"></a><span data-ttu-id="a900d-104">opzione/SAL</span><span class="sxs-lookup"><span data-stu-id="a900d-104">/sal switch</span></span>

<span data-ttu-id="a900d-105">L'opzione **/Sal** indica a MIDL di generare le annotazioni SAL nei file stub generati.</span><span class="sxs-lookup"><span data-stu-id="a900d-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="a900d-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="a900d-106">Switch Options</span></span>

<span data-ttu-id="a900d-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a900d-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a900d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a900d-108">Remarks</span></span>

<span data-ttu-id="a900d-109">MIDL contrassegna i parametri dei puntatori e delle matrici con le annotazioni che riflettono la descrizione del parametro nel file IDL come applicato da RPC e dal motore di marshalling del recapito.</span><span class="sxs-lookup"><span data-stu-id="a900d-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="a900d-110">MIDL non crea annotazioni per i parametri nei metodi di interfaccia contrassegnati con l'attributo [**\[ locale \]**](local.md), a meno che nella riga di comando non sia presente anche [**/SAL \_ local**](-sal-local.md) .</span><span class="sxs-lookup"><span data-stu-id="a900d-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="a900d-111">Per eseguire l'override dell'annotazione generata da MIDL, usare l'attributo [**\[ annotate \]**](annotate.md) .</span><span class="sxs-lookup"><span data-stu-id="a900d-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="a900d-112">Le annotazioni generate da MIDL sono sempre precedute dal prefisso \_ \_ RPC \_ e richiedono l'uso dell'intestazione **rpcsal. h** per convertire l'annotazione in annotazioni SAL standard.</span><span class="sxs-lookup"><span data-stu-id="a900d-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="a900d-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a900d-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a900d-114">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="a900d-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a900d-115">**/SAL \_ locale**</span><span class="sxs-lookup"><span data-stu-id="a900d-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="a900d-116">[**\[Annotare\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="a900d-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




