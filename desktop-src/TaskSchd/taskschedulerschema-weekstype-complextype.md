---
title: Tipo complesso weeksType
description: Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- Utilità di pianificazione di tipo complesso weeksType
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120883"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="7753a-104">Tipo complesso weeksType</span><span class="sxs-lookup"><span data-stu-id="7753a-104">weeksType Complex Type</span></span>

<span data-ttu-id="7753a-105">Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento [**week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7753a-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7753a-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7753a-106">Child elements</span></span>



| <span data-ttu-id="7753a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7753a-107">Element</span></span>                                                    | <span data-ttu-id="7753a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7753a-108">Type</span></span>                                                        | <span data-ttu-id="7753a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7753a-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="7753a-110">**Settimana**</span><span class="sxs-lookup"><span data-stu-id="7753a-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="7753a-111">**weekType**</span><span class="sxs-lookup"><span data-stu-id="7753a-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="7753a-112">Specifica la settimana in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="7753a-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7753a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7753a-113">Requirements</span></span>



| <span data-ttu-id="7753a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7753a-114">Requirement</span></span> | <span data-ttu-id="7753a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7753a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7753a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7753a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7753a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7753a-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7753a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7753a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7753a-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7753a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7753a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7753a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7753a-121">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7753a-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





