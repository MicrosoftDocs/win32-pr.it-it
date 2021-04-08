---
title: Gruppo actionGroup
description: Definisce il gruppo di azioni che possono essere eseguite da un'attività.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Utilità di pianificazione gruppo actionGroup
- Utilità di pianificazione actionGroup
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740834"
---
# <a name="actiongroup-group"></a><span data-ttu-id="2d6c3-105">Gruppo actionGroup</span><span class="sxs-lookup"><span data-stu-id="2d6c3-105">actionGroup Group</span></span>

<span data-ttu-id="2d6c3-106">Definisce il gruppo di azioni che possono essere eseguite da un'attività.</span><span class="sxs-lookup"><span data-stu-id="2d6c3-106">Defines the group of actions that a task can perform.</span></span>

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="2d6c3-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2d6c3-107">Child elements</span></span>



| <span data-ttu-id="2d6c3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d6c3-108">Element</span></span>                                                                    | <span data-ttu-id="2d6c3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d6c3-109">Type</span></span>                                                                       | <span data-ttu-id="2d6c3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d6c3-110">Description</span></span>                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="2d6c3-111">**Comgestore**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="2d6c3-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="2d6c3-113">Rappresenta un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="2d6c3-113">Represents an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="2d6c3-114">**Exec**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-114">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="2d6c3-115">**execType**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-115">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="2d6c3-116">Rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2d6c3-116">Represents an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="2d6c3-117">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-117">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="2d6c3-118">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-118">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="2d6c3-119">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2d6c3-119">Represents an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="2d6c3-120">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-120">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="2d6c3-121">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="2d6c3-121">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="2d6c3-122">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2d6c3-122">Represents an action that shows a message box.</span></span><br/>               |



## <a name="remarks"></a><span data-ttu-id="2d6c3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d6c3-123">Remarks</span></span>

<span data-ttu-id="2d6c3-124">Durante la lettura o la scrittura di codice XML, gli elementi definiti da questo gruppo sono gli elementi figlio dell'elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2d6c3-124">When reading or writing XML, the elements that are defined by this group are the child elements of the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d6c3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d6c3-125">Requirements</span></span>



| <span data-ttu-id="2d6c3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d6c3-126">Requirement</span></span> | <span data-ttu-id="2d6c3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2d6c3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d6c3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d6c3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2d6c3-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d6c3-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d6c3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d6c3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2d6c3-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d6c3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d6c3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d6c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d6c3-133">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2d6c3-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





