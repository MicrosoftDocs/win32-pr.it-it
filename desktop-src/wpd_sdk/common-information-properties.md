---
description: I dispositivi portatili Windows supportano le seguenti proprietà delle informazioni comuni.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Proprietà informazioni comuni (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330495"
---
# <a name="common-information-properties"></a><span data-ttu-id="e7b97-103">Proprietà informazioni comuni</span><span class="sxs-lookup"><span data-stu-id="e7b97-103">Common Information Properties</span></span>

<span data-ttu-id="e7b97-104">I dispositivi portatili Windows supportano le seguenti proprietà delle informazioni comuni.</span><span class="sxs-lookup"><span data-stu-id="e7b97-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="e7b97-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7b97-105">Property</span></span>                                      | <span data-ttu-id="e7b97-106">VarType</span><span class="sxs-lookup"><span data-stu-id="e7b97-106">VarType</span></span>        | <span data-ttu-id="e7b97-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7b97-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b97-108">**\_ \_ Note informative comuni di WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7b97-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="e7b97-109">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e7b97-110">Per gli appuntamenti, le attività e gli oggetti simili, questa proprietà contiene le note per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="e7b97-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="e7b97-111">**\_ \_ oggetto informazioni comuni \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="e7b97-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="e7b97-112">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e7b97-113">Valore che specifica il campo dell'oggetto di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7b97-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="e7b97-114">**\_testo del \_ corpo delle informazioni comuni \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7b97-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="e7b97-115">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="e7b97-116">Questa proprietà contiene il testo del corpo di un oggetto, in formato testo non crittografato o HTML.</span><span class="sxs-lookup"><span data-stu-id="e7b97-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="e7b97-117">**\_ \_ priorità delle informazioni comuni di WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7b97-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="e7b97-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-118">**VT\_UI4**</span></span>    | <span data-ttu-id="e7b97-119">Valore che specifica la priorità di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7b97-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="e7b97-120">0 indica la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="e7b97-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="e7b97-121">**Data/ora di \_ \_ inizio informazioni comuni \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7b97-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="e7b97-122">**\_Data VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-122">**VT\_DATE**</span></span>   | <span data-ttu-id="e7b97-123">Valore che specifica la data e l'ora in cui è pianificato l'avvio di un appuntamento, un'attività o un oggetto simile.</span><span class="sxs-lookup"><span data-stu-id="e7b97-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="e7b97-124">**Data/ora di \_ \_ fine informazioni comuni \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="e7b97-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="e7b97-125">**\_Data VT**</span><span class="sxs-lookup"><span data-stu-id="e7b97-125">**VT\_DATE**</span></span>   | <span data-ttu-id="e7b97-126">Valore che specifica la data e l'ora di fine pianificata per un appuntamento, un'attività o un oggetto simile.</span><span class="sxs-lookup"><span data-stu-id="e7b97-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e7b97-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b97-127">Requirements</span></span>



| <span data-ttu-id="e7b97-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b97-128">Requirement</span></span> | <span data-ttu-id="e7b97-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b97-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b97-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b97-130">Header</span></span><br/> | <dl> <span data-ttu-id="e7b97-131"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b97-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b97-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b97-133">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="e7b97-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




