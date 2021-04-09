---
title: tipo semplice guidType (Utilità di pianificazione)
description: Definisce il modello per i GUID validi.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- Utilità di pianificazione di tipo semplice guidType
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120899"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="b60f7-104">tipo semplice guidType (Utilità di pianificazione)</span><span class="sxs-lookup"><span data-stu-id="b60f7-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="b60f7-105">Definisce il modello per i GUID validi.</span><span class="sxs-lookup"><span data-stu-id="b60f7-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="b60f7-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="b60f7-106">Patterns</span></span>

<span data-ttu-id="b60f7-107">Il tipo semplice **guidType** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="b60f7-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="b60f7-108">Numero univoco a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="b60f7-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="b60f7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b60f7-109">Requirements</span></span>



| <span data-ttu-id="b60f7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b60f7-110">Requirement</span></span> | <span data-ttu-id="b60f7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b60f7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b60f7-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b60f7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b60f7-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b60f7-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b60f7-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b60f7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b60f7-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b60f7-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b60f7-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b60f7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b60f7-117">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b60f7-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b60f7-118">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b60f7-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





