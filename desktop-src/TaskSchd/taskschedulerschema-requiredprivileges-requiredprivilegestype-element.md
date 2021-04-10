---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Specifica i privilegi richiesti dall'attività.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Utilità di pianificazione elemento RequiredPrivileges
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121554"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a><span data-ttu-id="7085f-104">Elemento RequiredPrivileges (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="7085f-104">RequiredPrivileges (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="7085f-105">Specifica i privilegi richiesti dall'attività.</span><span class="sxs-lookup"><span data-stu-id="7085f-105">Specifies the privileges that are required by the task.</span></span>

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

<span data-ttu-id="7085f-106">L'elemento **RequiredPrivileges** è definito dal tipo complesso [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7085f-106">The **RequiredPrivileges** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7085f-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="7085f-107">Parent element</span></span>



| <span data-ttu-id="7085f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="7085f-108">Element</span></span>                                                                                  | <span data-ttu-id="7085f-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="7085f-109">Derived from</span></span>                                                           | <span data-ttu-id="7085f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7085f-110">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7085f-111">**Entità (principalType)**</span><span class="sxs-lookup"><span data-stu-id="7085f-111">**Principal (principalType)**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="7085f-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="7085f-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="7085f-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="7085f-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7085f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7085f-114">Remarks</span></span>

<span data-ttu-id="7085f-115">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="7085f-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="7085f-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="7085f-116">Examples</span></span>

<span data-ttu-id="7085f-117">Nel codice XML seguente viene definito utilizzando un identificatore di gruppo e i privilegi necessari.</span><span class="sxs-lookup"><span data-stu-id="7085f-117">The following XML defines using a group identifier and the required privileges.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="7085f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7085f-118">Requirements</span></span>



| <span data-ttu-id="7085f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7085f-119">Requirement</span></span> | <span data-ttu-id="7085f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7085f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7085f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7085f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7085f-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7085f-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7085f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7085f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7085f-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7085f-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7085f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7085f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7085f-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7085f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





