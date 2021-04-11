---
title: Tipo semplice weekType
description: Definisce i valori che possono essere utilizzati nell'elemento week.
ms.assetid: 83a525ae-020b-4528-9e14-1e7d9df7b8c0
keywords:
- Utilità di pianificazione di tipo semplice weekType
topic_type:
- apiref
api_name:
- weekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6513efe0fe0ef4fcbf6b849627d09ec9da6feb82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119383"
---
# <a name="weektype-simple-type"></a><span data-ttu-id="d4c05-104">Tipo semplice weekType</span><span class="sxs-lookup"><span data-stu-id="d4c05-104">weekType Simple Type</span></span>

<span data-ttu-id="d4c05-105">Definisce i valori che possono essere utilizzati nell'elemento [**week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4c05-105">Defines the values that can be used in the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="weekType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-4]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="d4c05-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="d4c05-106">Patterns</span></span>

<span data-ttu-id="d4c05-107">Il tipo semplice **weekType** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="d4c05-107">The **weekType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-4]|Last`

    <span data-ttu-id="d4c05-108">Specifica la prima per la quarta settimana del mese (1-4) o sempre l'ultima settimana del mese.</span><span class="sxs-lookup"><span data-stu-id="d4c05-108">Specifies the first through the fourth week of the month (1-4) or always the last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c05-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4c05-109">Requirements</span></span>



| <span data-ttu-id="d4c05-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c05-110">Requirement</span></span> | <span data-ttu-id="d4c05-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d4c05-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4c05-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4c05-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c05-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4c05-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4c05-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4c05-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c05-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4c05-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4c05-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4c05-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c05-117">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d4c05-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d4c05-118">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d4c05-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





