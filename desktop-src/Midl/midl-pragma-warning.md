---
title: midl_pragma attributo di avviso
description: Usare l' \_ opzione MIDL pragma warning per eseguire temporaneamente l'override del comportamento del messaggio di avviso di MIDL in fase di compilazione.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- attributo MIDL di avviso midl_pragma
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857225"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="2724e-104">\_attributo pragma warning di MIDL</span><span class="sxs-lookup"><span data-stu-id="2724e-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="2724e-105">Usare l'opzione **MIDL \_ pragma warning** per eseguire temporaneamente l'override del comportamento del messaggio di avviso di MIDL in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2724e-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="2724e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2724e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2724e-107">*\_opzione warning*</span><span class="sxs-lookup"><span data-stu-id="2724e-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="2724e-108">L'opzione di avviso può essere una delle seguenti: Disabilita, Abilita, valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2724e-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="2724e-109">*\_elenco messaggi*</span><span class="sxs-lookup"><span data-stu-id="2724e-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="2724e-110">Elenco di numeri di messaggio separati da spazi.</span><span class="sxs-lookup"><span data-stu-id="2724e-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2724e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2724e-111">Remarks</span></span>

<span data-ttu-id="2724e-112">Il pragma può essere usato come un pragma del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="2724e-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="2724e-113">Ovvero Disabilita, Abilita o restituisce il comportamento predefinito per un determinato avviso MIDL.</span><span class="sxs-lookup"><span data-stu-id="2724e-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="2724e-114">Esempi</span><span class="sxs-lookup"><span data-stu-id="2724e-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="2724e-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2724e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2724e-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="2724e-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




