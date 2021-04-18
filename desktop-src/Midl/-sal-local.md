---
title: /sal_local opzione
description: Il \_ commutire locale/Sal indica a MIDL di generare anche le annotazioni SAL per i parametri dei metodi di interfaccia contrassegnati come \ Local \. È necessario che sia presente anche l'opzione/Sal.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299092"
---
# <a name="sal_local-switch"></a><span data-ttu-id="88131-105">\_switch locale/SAL</span><span class="sxs-lookup"><span data-stu-id="88131-105">/sal\_local switch</span></span>

<span data-ttu-id="88131-106">Il commutire **\_ locale/Sal** indica a MIDL di generare anche le annotazioni SAL per i parametri dei metodi di interfaccia contrassegnati come [**\[ \] local**](local.md).</span><span class="sxs-lookup"><span data-stu-id="88131-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="88131-107">È necessario che sia presente anche l'opzione [**/Sal**](-sal.md) .</span><span class="sxs-lookup"><span data-stu-id="88131-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="88131-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="88131-108">Switch Options</span></span>

<span data-ttu-id="88131-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="88131-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="88131-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="88131-110">Remarks</span></span>

<span data-ttu-id="88131-111">Modifica il comportamento dell'opzione [**/Sal**](-sal.md) in modo da fornire anche le annotazioni sui parametri dei metodi di interfaccia contrassegnati con l'attributo [**\[ Local \]**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="88131-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="88131-112">Usare l'attributo [**\[ annota \]**](annotate.md)per eseguire l'override dell'annotazione generata da MIDL con una stringa di annotazione diversa.</span><span class="sxs-lookup"><span data-stu-id="88131-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="88131-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88131-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88131-114">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="88131-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="88131-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="88131-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="88131-116">[**\[Annotare\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="88131-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




