---
description: La struttura ADDRESSTABLE contiene una tabella di coppie di indirizzi.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Struttura ADDRESSTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485404"
---
# <a name="addresstable-structure"></a><span data-ttu-id="bd250-103">Struttura ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="bd250-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="bd250-104">La struttura **ADDRESSTABLE** contiene una tabella di coppie di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="bd250-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd250-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd250-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="bd250-106">Members</span><span class="sxs-lookup"><span data-stu-id="bd250-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd250-107">**nAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="bd250-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="bd250-108">Numero di coppie di indirizzi nella matrice **AddressPair** .</span><span class="sxs-lookup"><span data-stu-id="bd250-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="bd250-109">**nNonMacAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="bd250-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="bd250-110">Numero di coppie di indirizzi non MAC.</span><span class="sxs-lookup"><span data-stu-id="bd250-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="bd250-111">**AddressPair**</span><span class="sxs-lookup"><span data-stu-id="bd250-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="bd250-112">Matrice di coppie di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="bd250-112">Array of address pairs.</span></span> <span data-ttu-id="bd250-113">Si noti che è possibile archiviare fino a otto coppie di indirizzi per ogni struttura ADDRESSTABLE.</span><span class="sxs-lookup"><span data-stu-id="bd250-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd250-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd250-114">Remarks</span></span>

<span data-ttu-id="bd250-115">Usare questa struttura come parte del processo di creazione del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bd250-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="bd250-116">Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bd250-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd250-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd250-117">Requirements</span></span>



| <span data-ttu-id="bd250-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd250-118">Requirement</span></span> | <span data-ttu-id="bd250-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bd250-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bd250-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd250-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd250-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd250-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bd250-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd250-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd250-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd250-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bd250-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd250-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd250-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd250-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd250-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd250-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd250-127">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="bd250-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="bd250-128">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="bd250-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




