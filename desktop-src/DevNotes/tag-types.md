---
description: Descrive il tipo di dati del valore associato a un TAG.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Tipi di TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225561"
---
# <a name="tag-types"></a><span data-ttu-id="533c7-103">Tipi di TAG</span><span class="sxs-lookup"><span data-stu-id="533c7-103">TAG Types</span></span>

<span data-ttu-id="533c7-104">Descrive il tipo di dati del valore associato a un TAG.</span><span class="sxs-lookup"><span data-stu-id="533c7-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="533c7-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="533c7-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="533c7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="533c7-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="533c7-107"><dt>**Tag \_ di Digitare \_ null**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="533c7-108">Al TAG non è associato alcun valore.</span><span class="sxs-lookup"><span data-stu-id="533c7-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="533c7-109"><dt>**Tag \_ di Digitare \_ byte**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="533c7-110">Valore **byte** .</span><span class="sxs-lookup"><span data-stu-id="533c7-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="533c7-111"><dt>**Tag \_ di Digitare \_ Word**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="533c7-112">Valore di **parola** .</span><span class="sxs-lookup"><span data-stu-id="533c7-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="533c7-113"><dt>**Tag \_ di Digitare \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="533c7-114">Valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="533c7-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="533c7-115"><dt>**Tag \_ di Digitare \_ QWORD**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="533c7-116">Valore **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="533c7-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="533c7-117"><dt>**Tag \_ di Digitare \_ STRINGREF**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="533c7-118">Valore stringa in formato token.</span><span class="sxs-lookup"><span data-stu-id="533c7-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="533c7-119"><dt>**Tag \_ di TIPO \_ elenco**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="533c7-120">Elenco di valori di TAG.</span><span class="sxs-lookup"><span data-stu-id="533c7-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="533c7-121"><dt>**Tag \_ di DIGITARE la \_ stringa**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="533c7-122">Valore stringa.</span><span class="sxs-lookup"><span data-stu-id="533c7-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="533c7-123"><dt>**Tag \_ di Digitare \_ Binary**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="533c7-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="533c7-124">Valore binario.</span><span class="sxs-lookup"><span data-stu-id="533c7-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="533c7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="533c7-125">Requirements</span></span>



| <span data-ttu-id="533c7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="533c7-126">Requirement</span></span> | <span data-ttu-id="533c7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="533c7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="533c7-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="533c7-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="533c7-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="533c7-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="533c7-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="533c7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="533c7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="533c7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533c7-133">**TAG**</span><span class="sxs-lookup"><span data-stu-id="533c7-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="533c7-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="533c7-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="533c7-135">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="533c7-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




