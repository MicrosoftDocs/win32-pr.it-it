---
title: Description (registrationInfoType)-elemento
description: Specifica la descrizione dell'attività.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Elemento Description Utilità di pianificazione
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740823"
---
# <a name="description-registrationinfotype-element"></a><span data-ttu-id="b9712-104">Description (registrationInfoType)-elemento</span><span class="sxs-lookup"><span data-stu-id="b9712-104">Description (registrationInfoType) Element</span></span>

<span data-ttu-id="b9712-105">Specifica la descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b9712-105">Specifies the description of the task.</span></span>

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="b9712-106">L'elemento **Description** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b9712-106">The **Description** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b9712-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b9712-107">Parent element</span></span>



| <span data-ttu-id="b9712-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b9712-108">Element</span></span>                                                                           | <span data-ttu-id="b9712-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="b9712-109">Derived from</span></span>                                                                         | <span data-ttu-id="b9712-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9712-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9712-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b9712-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="b9712-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="b9712-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="b9712-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b9712-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9712-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9712-114">Remarks</span></span>

<span data-ttu-id="b9712-115">Per lo sviluppo di script, la descrizione di un'attività viene specificata utilizzando la proprietà [**RegistrationInfo. Description**](registrationinfo-description.md) .</span><span class="sxs-lookup"><span data-stu-id="b9712-115">For scripting development, the description of a task is specified using the [**RegistrationInfo.Description**](registrationinfo-description.md) property.</span></span>

<span data-ttu-id="b9712-116">Per lo sviluppo in C++, la descrizione di un'attività viene specificata tramite la proprietà [**IRegistrationInfo::D Descrizione**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .</span><span class="sxs-lookup"><span data-stu-id="b9712-116">For C++ development, the description of a task is specified using the [**IRegistrationInfo::Description**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9712-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9712-117">Requirements</span></span>



| <span data-ttu-id="b9712-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9712-118">Requirement</span></span> | <span data-ttu-id="b9712-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b9712-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9712-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9712-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9712-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9712-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9712-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9712-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9712-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9712-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9712-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9712-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9712-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b9712-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b9712-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="b9712-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





