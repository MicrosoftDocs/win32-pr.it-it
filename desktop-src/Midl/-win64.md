---
title: opzione/Win64
description: L'opzione/Win64 indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 64 bit. Nota Questa opzione è obsoleta.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64 switch MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333692"
---
# <a name="win64-switch"></a><span data-ttu-id="d2eb1-104">opzione/Win64</span><span class="sxs-lookup"><span data-stu-id="d2eb1-104">/win64 switch</span></span>

<span data-ttu-id="d2eb1-105">L'opzione **/Win64** indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="d2eb1-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="d2eb1-106">Questa opzione è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d2eb1-106">This switch is obsolete.</span></span> <span data-ttu-id="d2eb1-107">Usare invece l'opzione [**/ia64**](-ia64.md) o [**/amd64**](-amd64.md) .</span><span class="sxs-lookup"><span data-stu-id="d2eb1-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="d2eb1-108">L'opzione **/Win64** equivale all'opzione **/ia64** .</span><span class="sxs-lookup"><span data-stu-id="d2eb1-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="d2eb1-109">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="d2eb1-109">Switch Options</span></span>

<span data-ttu-id="d2eb1-110">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="d2eb1-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2eb1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2eb1-111">Remarks</span></span>

<span data-ttu-id="d2eb1-112">L'opzione **/Win64** equivale a impostare l'opzione [**/ENV**](-env.md) su Win64.</span><span class="sxs-lookup"><span data-stu-id="d2eb1-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="d2eb1-113">Non è possibile usare MIDL.exe per produrre un TLB a 64 bit in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d2eb1-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d2eb1-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2eb1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2eb1-115">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="d2eb1-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="d2eb1-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="d2eb1-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="d2eb1-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="d2eb1-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




