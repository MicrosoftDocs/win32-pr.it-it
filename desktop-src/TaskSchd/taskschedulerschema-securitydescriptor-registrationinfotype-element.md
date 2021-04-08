---
title: Elemento SecurityDescriptor (registrationInfoType)
description: Specifica il descrittore di sicurezza dell'attività.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Utilità di pianificazione elemento SecurityDescriptor
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048036"
---
# <a name="securitydescriptor-registrationinfotype-element"></a><span data-ttu-id="b2b5a-104">Elemento SecurityDescriptor (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="b2b5a-104">SecurityDescriptor (registrationInfoType) Element</span></span>

<span data-ttu-id="b2b5a-105">Specifica il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-105">Specifies the security descriptor of the task.</span></span>

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

<span data-ttu-id="b2b5a-106">L'elemento **securityDescriptor** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b5a-106">The **SecurityDescriptor** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b2b5a-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b2b5a-107">Parent element</span></span>



| <span data-ttu-id="b2b5a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2b5a-108">Element</span></span>                                                                           | <span data-ttu-id="b2b5a-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="b2b5a-109">Derived from</span></span>                                                                         | <span data-ttu-id="b2b5a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2b5a-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2b5a-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="b2b5a-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="b2b5a-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="b2b5a-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b2b5a-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b2b5a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2b5a-114">Remarks</span></span>

<span data-ttu-id="b2b5a-115">Per lo sviluppo di script, il descrittore di sicurezza di un'attività viene specificato mediante la proprietà [**RegistrationInfo. SecurityDescriptor**](registrationinfo-securitydescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b5a-115">For scripting development, the security descriptor of a task is specified using the [**RegistrationInfo.SecurityDescriptor**](registrationinfo-securitydescriptor.md) property.</span></span>

<span data-ttu-id="b2b5a-116">Per lo sviluppo in C++, il descrittore di sicurezza di un'attività viene specificato mediante la proprietà [**IRegistrationInfo:: securityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b2b5a-116">For C++ development, the security descriptor of a task is specified using the [**IRegistrationInfo::SecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b5a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2b5a-117">Requirements</span></span>



| <span data-ttu-id="b2b5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b5a-118">Requirement</span></span> | <span data-ttu-id="b2b5a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b2b5a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2b5a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b5a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2b5a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2b5a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2b5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b5a-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2b5a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2b5a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2b5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b5a-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b2b5a-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b2b5a-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b2b5a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





