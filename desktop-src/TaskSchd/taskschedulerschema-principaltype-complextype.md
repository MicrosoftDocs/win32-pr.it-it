---
title: Tipo complesso principalType
description: Definisce l'attributo, gli elementi figlio e le informazioni di sequenziazione per l'elemento Principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- Utilità di pianificazione di tipo complesso principalType
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478167"
---
# <a name="principaltype-complex-type"></a><span data-ttu-id="a40c3-104">Tipo complesso principalType</span><span class="sxs-lookup"><span data-stu-id="a40c3-104">principalType Complex Type</span></span>

<span data-ttu-id="a40c3-105">Definisce l'attributo, gli elementi figlio e le informazioni di sequenziazione per l'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a40c3-105">Defines the attribute, child elements, and sequencing information for the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element.</span></span>

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a40c3-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a40c3-106">Child elements</span></span>



| <span data-ttu-id="a40c3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a40c3-107">Element</span></span>                                                                                             | <span data-ttu-id="a40c3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a40c3-108">Type</span></span>                                                                                     | <span data-ttu-id="a40c3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40c3-109">Description</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a40c3-110">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a40c3-110">**DisplayName**</span></span>](taskschedulerschema-displayname-principaltype-element.md)                        | <span data-ttu-id="a40c3-111">string</span><span class="sxs-lookup"><span data-stu-id="a40c3-111">string</span></span>                                                                                   | <span data-ttu-id="a40c3-112">Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a40c3-112">Specifies the name of the principal that is displayed in the Task Scheduler user interface (UI).</span></span><br/>                 |
| [<span data-ttu-id="a40c3-113">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="a40c3-113">**GroupId**</span></span>](taskschedulerschema-groupid-principaltype-element.md)                                | [<span data-ttu-id="a40c3-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="a40c3-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="a40c3-115">Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="a40c3-115">Specifies the identifier of the user group that is required to run tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="a40c3-116">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-116">**LogonType**</span></span>](taskschedulerschema-logontype-principaltype-element.md)                            | [<span data-ttu-id="a40c3-117">**logonType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-117">**logonType**</span></span>](taskschedulerschema-logontype-simpletype.md)                            | <span data-ttu-id="a40c3-118">Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="a40c3-118">Specifies the security logon method that is required to run tasks that are associated with the principal.</span></span><br/>        |
| [<span data-ttu-id="a40c3-119">**ProcessTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-119">**ProcessTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [<span data-ttu-id="a40c3-120">**processTokenSidType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-120">**processTokenSidType**</span></span>](taskschedulerschema-processtokensidtype-simpletype.md)        | <span data-ttu-id="a40c3-121">Specifica i tipi di ID di sicurezza (SID) del processo che possono essere utilizzati dalle attività.</span><span class="sxs-lookup"><span data-stu-id="a40c3-121">Specifies the types of process security identifier (SID) that can be used by tasks.</span></span><br/>                              |
| [<span data-ttu-id="a40c3-122">**RequiredPrivileges**</span><span class="sxs-lookup"><span data-stu-id="a40c3-122">**RequiredPrivileges**</span></span>](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [<span data-ttu-id="a40c3-123">**requiredPrivilegesType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-123">**requiredPrivilegesType**</span></span>](taskschedulerschema-requiredprivilegestype-complextype.md) | <span data-ttu-id="a40c3-124">Specifica i privilegi necessari per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="a40c3-124">Specifies the required privileges to run the task.</span></span><br/>                                                               |
| [<span data-ttu-id="a40c3-125">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="a40c3-125">**RunLevel**</span></span>](taskschedulerschema-runlevel-principaltype-element.md)                              | [<span data-ttu-id="a40c3-126">**runLevelType**</span><span class="sxs-lookup"><span data-stu-id="a40c3-126">**runLevelType**</span></span>](taskschedulerschema-runleveltype-simpletype.md)                      | <span data-ttu-id="a40c3-127">Specifica il livello di autorizzazione in cui verrà eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="a40c3-127">Specifies the permission level that the task will be run at.</span></span><br/>                                                     |
| [<span data-ttu-id="a40c3-128">**UserId**</span><span class="sxs-lookup"><span data-stu-id="a40c3-128">**UserId**</span></span>](taskschedulerschema-userid-principaltype-element.md)                                  | [<span data-ttu-id="a40c3-129">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="a40c3-129">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                  | <span data-ttu-id="a40c3-130">Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="a40c3-130">Specifies the user identifier that is required to run tasks that are associated with the principal.</span></span><br/>              |



## <a name="attributes"></a><span data-ttu-id="a40c3-131">Attributi</span><span class="sxs-lookup"><span data-stu-id="a40c3-131">Attributes</span></span>



| <span data-ttu-id="a40c3-132">Nome</span><span class="sxs-lookup"><span data-stu-id="a40c3-132">Name</span></span> | <span data-ttu-id="a40c3-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="a40c3-133">Type</span></span> | <span data-ttu-id="a40c3-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40c3-134">Description</span></span>                                           |
|------|------|-------------------------------------------------------|
| <span data-ttu-id="a40c3-135">id</span><span class="sxs-lookup"><span data-stu-id="a40c3-135">id</span></span>   | <span data-ttu-id="a40c3-136">ID</span><span class="sxs-lookup"><span data-stu-id="a40c3-136">ID</span></span>   | <span data-ttu-id="a40c3-137">Specifica l'identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="a40c3-137">Specifies the identifier of the principal.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a40c3-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a40c3-138">Requirements</span></span>



| <span data-ttu-id="a40c3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40c3-139">Requirement</span></span> | <span data-ttu-id="a40c3-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a40c3-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a40c3-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40c3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a40c3-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a40c3-142">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a40c3-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40c3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a40c3-144">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a40c3-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a40c3-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a40c3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40c3-146">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a40c3-146">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a40c3-147">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a40c3-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





