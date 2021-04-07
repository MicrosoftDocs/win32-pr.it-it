---
title: Tipo semplice priorityType
description: Definisce i valori minimo e massimo per l'elemento Priority (settingsType).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- Utilità di pianificazione di tipo semplice priorityType
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048607"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="20cae-104">Tipo semplice priorityType</span><span class="sxs-lookup"><span data-stu-id="20cae-104">priorityType Simple Type</span></span>

<span data-ttu-id="20cae-105">Definisce i valori minimo e massimo per l'elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="20cae-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="20cae-106">Valori di enumerazione</span><span class="sxs-lookup"><span data-stu-id="20cae-106">Enumeration values</span></span>

<span data-ttu-id="20cae-107">Il tipo semplice **priorityType** definisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20cae-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="20cae-108">Valore</span><span class="sxs-lookup"><span data-stu-id="20cae-108">Value</span></span> | <span data-ttu-id="20cae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20cae-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="20cae-110">0</span><span class="sxs-lookup"><span data-stu-id="20cae-110">0</span></span>     | <span data-ttu-id="20cae-111">Numero intero minimo consentito.</span><span class="sxs-lookup"><span data-stu-id="20cae-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="20cae-112">10</span><span class="sxs-lookup"><span data-stu-id="20cae-112">10</span></span>    | <span data-ttu-id="20cae-113">Numero intero massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="20cae-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="20cae-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20cae-114">Requirements</span></span>



| <span data-ttu-id="20cae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cae-115">Requirement</span></span> | <span data-ttu-id="20cae-116">Valore</span><span class="sxs-lookup"><span data-stu-id="20cae-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20cae-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20cae-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20cae-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="20cae-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20cae-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20cae-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20cae-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20cae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cae-122">Tipi semplici dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="20cae-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="20cae-123">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="20cae-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





