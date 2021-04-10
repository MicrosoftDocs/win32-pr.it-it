---
title: Elemento date (registrationInfoType)
description: Specifica la data e l'ora di registrazione dell'attività.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Utilità di pianificazione elemento Data
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120407"
---
# <a name="date-registrationinfotype-element"></a><span data-ttu-id="06352-104">Elemento date (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="06352-104">Date (registrationInfoType) Element</span></span>

<span data-ttu-id="06352-105">Specifica la data e l'ora di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="06352-105">Specifies the date and time when the task is registered.</span></span>

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

<span data-ttu-id="06352-106">L'elemento **date** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="06352-106">The **Date** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="06352-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="06352-107">Parent element</span></span>



| <span data-ttu-id="06352-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="06352-108">Element</span></span>                                                                           | <span data-ttu-id="06352-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="06352-109">Derived from</span></span>                                                                         | <span data-ttu-id="06352-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06352-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06352-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="06352-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="06352-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="06352-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="06352-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="06352-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06352-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="06352-114">Remarks</span></span>

<span data-ttu-id="06352-115">Per lo sviluppo di script, la data di registrazione di un'attività viene specificata utilizzando la proprietà [**RegistrationInfo. date**](registrationinfo-date.md) .</span><span class="sxs-lookup"><span data-stu-id="06352-115">For scripting development, the registration date of a task is specified using the [**RegistrationInfo.Date**](registrationinfo-date.md) property.</span></span>

<span data-ttu-id="06352-116">Per lo sviluppo in C++, la data di registrazione di un'attività viene specificata tramite la proprietà [**IRegistrationInfo::D ate**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .</span><span class="sxs-lookup"><span data-stu-id="06352-116">For C++ development, the registration date of a task is specified using the [**IRegistrationInfo::Date**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="06352-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06352-117">Requirements</span></span>



| <span data-ttu-id="06352-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="06352-118">Requirement</span></span> | <span data-ttu-id="06352-119">Valore</span><span class="sxs-lookup"><span data-stu-id="06352-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06352-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06352-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06352-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06352-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06352-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06352-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06352-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06352-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06352-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06352-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06352-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="06352-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="06352-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="06352-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





