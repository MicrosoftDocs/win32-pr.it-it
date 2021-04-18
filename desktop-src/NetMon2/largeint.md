---
description: Il tipo di dati LARGEINT definisce un \_ valore Integer grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302766"
---
# <a name="largeint"></a><span data-ttu-id="2bd4d-103">LARGEINT</span><span class="sxs-lookup"><span data-stu-id="2bd4d-103">LARGEINT</span></span>

<span data-ttu-id="2bd4d-104">Il tipo di dati **largeInt** definisce un valore [**\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .</span><span class="sxs-lookup"><span data-stu-id="2bd4d-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="2bd4d-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd4d-105">Remarks</span></span>

<span data-ttu-id="2bd4d-106">Il membro **lpLargeIntTable** della struttura del [**set**](set.md) punta a una matrice di strutture **set** che definiscono uno o più valori LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="2bd4d-107">Quando questo tipo di struttura **set** viene specificato, Network Monitor visualizza una delle etichette seguenti con ogni valore largeInt trovato nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="2bd4d-108">Corrisponde al valore impostato.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-108">Matches set value.</span></span> <span data-ttu-id="2bd4d-109">Il valore LARGEINT è incluso nel set.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="2bd4d-110">Valore impostato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-110">Unknown set value.</span></span> <span data-ttu-id="2bd4d-111">Il valore LARGEINT non è incluso nel set.</span><span class="sxs-lookup"><span data-stu-id="2bd4d-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd4d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd4d-112">Requirements</span></span>



| <span data-ttu-id="2bd4d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd4d-113">Requirement</span></span> | <span data-ttu-id="2bd4d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd4d-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd4d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd4d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd4d-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd4d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2bd4d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd4d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd4d-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bd4d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2bd4d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd4d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd4d-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd4d-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd4d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd4d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd4d-122">SET</span><span class="sxs-lookup"><span data-stu-id="2bd4d-122">SET</span></span>](set.md)
</dt> </dl>

 

