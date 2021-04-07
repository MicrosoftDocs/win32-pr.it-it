---
title: Elemento GroupId (principalType)
description: Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Utilità di pianificazione elemento GroupId
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048627"
---
# <a name="groupid-principaltype-element"></a><span data-ttu-id="472d3-104">Elemento GroupId (principalType)</span><span class="sxs-lookup"><span data-stu-id="472d3-104">GroupId (principalType) Element</span></span>

<span data-ttu-id="472d3-105">Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="472d3-105">Specifies the identifier of the user group required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="472d3-106">L'elemento **GroupID** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="472d3-106">The **GroupId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="472d3-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="472d3-107">Parent element</span></span>



| <span data-ttu-id="472d3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="472d3-108">Element</span></span>                                                                  | <span data-ttu-id="472d3-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="472d3-109">Derived from</span></span>                                                           | <span data-ttu-id="472d3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="472d3-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="472d3-111">**Principale**</span><span class="sxs-lookup"><span data-stu-id="472d3-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="472d3-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="472d3-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="472d3-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="472d3-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="472d3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="472d3-114">Remarks</span></span>

<span data-ttu-id="472d3-115">Non è possibile specificare contemporaneamente un identificatore di gruppo e un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="472d3-115">You cannot specify a group identifier and a user identifier at the same time.</span></span> <span data-ttu-id="472d3-116">Specificare gli elementi [**userid**](taskschedulerschema-userid-principaltype-element.md) o **GroupID** , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="472d3-116">Specify either the [**UserId**](taskschedulerschema-userid-principaltype-element.md) or **GroupId** elements, but not both.</span></span>

<span data-ttu-id="472d3-117">Per lo sviluppo di script, l'identificatore di gruppo dell'entità viene specificato utilizzando la proprietà [**Principal. GroupID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="472d3-117">For script development, the group identifier of the principal is specified using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="472d3-118">Per lo sviluppo in C++, l'identificatore di gruppo dell'entità viene specificato tramite la proprietà [**IPrincipal:: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .</span><span class="sxs-lookup"><span data-stu-id="472d3-118">For C++ development, the group identifier of the principal is specified using the [**IPrincipal::GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="472d3-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="472d3-119">Examples</span></span>

<span data-ttu-id="472d3-120">Per un esempio completo del codice XML per un'attività che usa questo elemento, vedere [esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="472d3-120">For a complete example of the XML for a task that uses this element, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="472d3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="472d3-121">Requirements</span></span>



| <span data-ttu-id="472d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="472d3-122">Requirement</span></span> | <span data-ttu-id="472d3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="472d3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="472d3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="472d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="472d3-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="472d3-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="472d3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="472d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="472d3-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="472d3-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="472d3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="472d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472d3-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="472d3-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





