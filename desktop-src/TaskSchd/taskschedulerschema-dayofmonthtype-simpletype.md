---
title: Tipo semplice dayOfMonthType
description: Definisce i valori possibili per specificare un giorno del mese.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- Utilità di pianificazione di tipo semplice dayOfMonthType
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517505"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="488ee-104">Tipo semplice dayOfMonthType</span><span class="sxs-lookup"><span data-stu-id="488ee-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="488ee-105">Definisce i valori possibili per specificare un giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="488ee-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="488ee-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="488ee-106">Patterns</span></span>

<span data-ttu-id="488ee-107">Il tipo semplice **dayOfMonthType** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="488ee-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="488ee-108">Specifica il primo e il 31 ° giorno del mese o sempre l'ultimo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="488ee-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="488ee-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="488ee-109">Requirements</span></span>



| <span data-ttu-id="488ee-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="488ee-110">Requirement</span></span> | <span data-ttu-id="488ee-111">Valore</span><span class="sxs-lookup"><span data-stu-id="488ee-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="488ee-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="488ee-112">Minimum supported client</span></span><br/> | <span data-ttu-id="488ee-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="488ee-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="488ee-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="488ee-114">Minimum supported server</span></span><br/> | <span data-ttu-id="488ee-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="488ee-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="488ee-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="488ee-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488ee-117">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="488ee-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="488ee-118">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="488ee-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





