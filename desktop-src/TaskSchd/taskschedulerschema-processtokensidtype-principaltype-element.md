---
title: Elemento ProcessTokenSidType (principalType)
description: Specifica il tipo di identificazione di sicurezza del processo (SID) dell'attività.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Utilità di pianificazione elemento ProcessTokenSidType
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120406"
---
# <a name="processtokensidtype-principaltype-element"></a><span data-ttu-id="4acfb-104">Elemento ProcessTokenSidType (principalType)</span><span class="sxs-lookup"><span data-stu-id="4acfb-104">ProcessTokenSidType (principalType) Element</span></span>

<span data-ttu-id="4acfb-105">Specifica il tipo di identificazione di sicurezza del processo (SID) dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4acfb-105">Specifies the process security identify (SID) type of the task.</span></span>

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="4acfb-106">L'elemento **ProcessTokenSidType** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4acfb-106">The **ProcessTokenSidType** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4acfb-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4acfb-107">Parent element</span></span>



| <span data-ttu-id="4acfb-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4acfb-108">Element</span></span>                                                                  | <span data-ttu-id="4acfb-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4acfb-109">Derived from</span></span>                                                           | <span data-ttu-id="4acfb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4acfb-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4acfb-111">**Principale**</span><span class="sxs-lookup"><span data-stu-id="4acfb-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="4acfb-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="4acfb-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="4acfb-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="4acfb-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4acfb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4acfb-114">Remarks</span></span>

<span data-ttu-id="4acfb-115">Per lo sviluppo in C++, il tipo di SID del processo viene specificato tramite la proprietà [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .</span><span class="sxs-lookup"><span data-stu-id="4acfb-115">For C++ development, the process SID type is specified by using the [**IPrincipal2::ProcessTokenSidType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) property.</span></span>

## <a name="examples"></a><span data-ttu-id="4acfb-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4acfb-116">Examples</span></span>

<span data-ttu-id="4acfb-117">Nel codice XML seguente viene definito il tipo di SID di processo dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4acfb-117">The following XML defines the process SID type of the task.</span></span>


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a><span data-ttu-id="4acfb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4acfb-118">Requirements</span></span>



| <span data-ttu-id="4acfb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4acfb-119">Requirement</span></span> | <span data-ttu-id="4acfb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4acfb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4acfb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4acfb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4acfb-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4acfb-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4acfb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4acfb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4acfb-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4acfb-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4acfb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4acfb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4acfb-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4acfb-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





