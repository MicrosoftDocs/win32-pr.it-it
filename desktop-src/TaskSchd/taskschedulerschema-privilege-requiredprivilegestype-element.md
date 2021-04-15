---
title: Elemento Privilege (requiredPrivilegesType)
description: Specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Elemento Privilege Utilità di pianificazione
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478388"
---
# <a name="privilege-requiredprivilegestype-element"></a><span data-ttu-id="941d1-104">Elemento Privilege (requiredPrivilegesType)</span><span class="sxs-lookup"><span data-stu-id="941d1-104">Privilege (requiredPrivilegesType) Element</span></span>

<span data-ttu-id="941d1-105">Specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="941d1-105">Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

<span data-ttu-id="941d1-106">L'elemento **Privilege** è definito dal tipo complesso [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="941d1-106">The **Privilege** element is defined by the [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="941d1-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="941d1-107">Parent element</span></span>



| <span data-ttu-id="941d1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="941d1-108">Element</span></span>                                                                                             | <span data-ttu-id="941d1-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="941d1-109">Derived from</span></span>                                                                             | <span data-ttu-id="941d1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="941d1-110">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="941d1-111">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="941d1-111">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="941d1-112">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="941d1-112">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="941d1-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="941d1-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="941d1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="941d1-114">Remarks</span></span>

<span data-ttu-id="941d1-115">Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .</span><span class="sxs-lookup"><span data-stu-id="941d1-115">For C++ development, this information is accessed through the [**IPrincipal2::RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) property.</span></span>

## <a name="examples"></a><span data-ttu-id="941d1-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="941d1-116">Examples</span></span>

<span data-ttu-id="941d1-117">Nel codice XML seguente viene definito un elemento Settings che specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="941d1-117">The following XML defines a settings element that specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span>


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
        
```



## <a name="requirements"></a><span data-ttu-id="941d1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="941d1-118">Requirements</span></span>



| <span data-ttu-id="941d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="941d1-119">Requirement</span></span> | <span data-ttu-id="941d1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="941d1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="941d1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="941d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="941d1-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="941d1-122">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="941d1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="941d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="941d1-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="941d1-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="941d1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="941d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="941d1-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="941d1-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





