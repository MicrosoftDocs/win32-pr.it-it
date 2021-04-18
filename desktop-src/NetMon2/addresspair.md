---
description: La struttura ADDRESSPAIR costruisce un filtro di acquisizione.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Struttura ADDRESSPAIR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314187"
---
# <a name="addresspair-structure"></a><span data-ttu-id="817ea-103">Struttura ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="817ea-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="817ea-104">La struttura **ADDRESSPAIR** costruisce un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="817ea-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="817ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="817ea-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="817ea-106">Members</span><span class="sxs-lookup"><span data-stu-id="817ea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="817ea-107">**AddressFlags**</span><span class="sxs-lookup"><span data-stu-id="817ea-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="817ea-108">Flag che descrivono gli indirizzi utilizzati da un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="817ea-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="817ea-109">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="817ea-109">See Remarks for more information.</span></span>



| <span data-ttu-id="817ea-110">Valore</span><span class="sxs-lookup"><span data-stu-id="817ea-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="817ea-111">Significato</span><span class="sxs-lookup"><span data-stu-id="817ea-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="817ea-112"><dt>**flag di indirizzo \_ \_ corrispondenti all' \_ ora legale**</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="817ea-113">Corrisponde all'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="817ea-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="817ea-114"><dt>**flag di indirizzo \_ \_ corrispondenti a \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="817ea-115">Corrisponde all'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="817ea-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="817ea-116"><dt>**flag di indirizzo \_ \_ esclusi**</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="817ea-117">Esclude il frame se viene trovato questo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="817ea-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="817ea-118"><dt>**INDIRIZZI \_ flag \_ del \_ gruppo \_ di indirizzi DST**</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="817ea-119">Corrisponde solo al bit del gruppo.</span><span class="sxs-lookup"><span data-stu-id="817ea-119">Matches group bit only.</span></span> <span data-ttu-id="817ea-120">Usare questa per i messaggi di tipo broadcast.</span><span class="sxs-lookup"><span data-stu-id="817ea-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="817ea-121"><dt>**i \_ flag di indirizzo \_ corrispondono a \_ entrambi**</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="817ea-122">Corrisponde a indirizzi di destinazione e di origine.</span><span class="sxs-lookup"><span data-stu-id="817ea-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="817ea-123">**NalReserved**</span><span class="sxs-lookup"><span data-stu-id="817ea-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="817ea-124">Questa operazione è riservata.</span><span class="sxs-lookup"><span data-stu-id="817ea-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="817ea-125">**DstAddress**</span><span class="sxs-lookup"><span data-stu-id="817ea-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="817ea-126">Indirizzo di destinazione dell'elemento della coppia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="817ea-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="817ea-127">**SrcAddress**</span><span class="sxs-lookup"><span data-stu-id="817ea-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="817ea-128">Indirizzo di origine dell'elemento della coppia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="817ea-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="817ea-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="817ea-129">Remarks</span></span>

<span data-ttu-id="817ea-130">I flag del membro **AddressFlags** possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="817ea-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="817ea-131">Ad esempio, l'impostazione seguente esclude il frame se viene rilevato l'indirizzo di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="817ea-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="817ea-132">Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="817ea-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="817ea-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="817ea-133">Requirements</span></span>



| <span data-ttu-id="817ea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="817ea-134">Requirement</span></span> | <span data-ttu-id="817ea-135">Valore</span><span class="sxs-lookup"><span data-stu-id="817ea-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="817ea-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="817ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="817ea-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="817ea-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="817ea-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="817ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="817ea-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="817ea-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="817ea-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="817ea-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="817ea-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="817ea-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="817ea-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="817ea-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817ea-143">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="817ea-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




