---
title: Tipo complesso requiredPrivilegesType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RequiredPrivileges (requiredPrivilegesType).
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- Utilità di pianificazione di tipo complesso requiredPrivilegesType
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479228"
---
# <a name="requiredprivilegestype-complex-type"></a><span data-ttu-id="137b3-104">Tipo complesso requiredPrivilegesType</span><span class="sxs-lookup"><span data-stu-id="137b3-104">requiredPrivilegesType Complex Type</span></span>

<span data-ttu-id="137b3-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="137b3-105">Defines the child elements and sequencing information for the [**RequiredPrivileges (requiredPrivilegesType)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) element.</span></span>

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="137b3-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="137b3-106">Child elements</span></span>



| <span data-ttu-id="137b3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="137b3-107">Element</span></span>                                                                           | <span data-ttu-id="137b3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="137b3-108">Type</span></span>                                                                  | <span data-ttu-id="137b3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="137b3-109">Description</span></span>                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="137b3-110">**Privilegio**</span><span class="sxs-lookup"><span data-stu-id="137b3-110">**Privilege**</span></span>](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [<span data-ttu-id="137b3-111">**privilegeType**</span><span class="sxs-lookup"><span data-stu-id="137b3-111">**privilegeType**</span></span>](taskschedulerschema-privilegetype-simpletype.md) | <span data-ttu-id="137b3-112">Specifica i privilegi necessari per l'attività.</span><span class="sxs-lookup"><span data-stu-id="137b3-112">Specifies the required privileges of the task.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="137b3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="137b3-113">Requirements</span></span>



| <span data-ttu-id="137b3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="137b3-114">Requirement</span></span> | <span data-ttu-id="137b3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="137b3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="137b3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="137b3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="137b3-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="137b3-117">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="137b3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="137b3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="137b3-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="137b3-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="137b3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="137b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137b3-121">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="137b3-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="137b3-122">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="137b3-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





