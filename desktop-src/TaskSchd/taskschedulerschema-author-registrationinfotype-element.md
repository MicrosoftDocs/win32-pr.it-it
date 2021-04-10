---
title: Elemento Author (registrationInfoType)
description: Specifica l'autore dell'attività.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Elemento Author Utilità di pianificazione
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964438"
---
# <a name="author-registrationinfotype-element"></a><span data-ttu-id="0f22e-104">Elemento Author (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="0f22e-104">Author (registrationInfoType) Element</span></span>

<span data-ttu-id="0f22e-105">Specifica l'autore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0f22e-105">Specifies the author of the task.</span></span>

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="0f22e-106">L'elemento **Author** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0f22e-106">The **Author** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0f22e-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="0f22e-107">Parent element</span></span>



| <span data-ttu-id="0f22e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f22e-108">Element</span></span>                                                                           | <span data-ttu-id="0f22e-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="0f22e-109">Derived from</span></span>                                                                         | <span data-ttu-id="0f22e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f22e-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f22e-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="0f22e-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="0f22e-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="0f22e-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="0f22e-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0f22e-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0f22e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f22e-114">Remarks</span></span>

<span data-ttu-id="0f22e-115">Per lo sviluppo di script, l'autore dell'attività viene specificato utilizzando la proprietà [**RegistrationInfo. Author**](registrationinfo-author.md) .</span><span class="sxs-lookup"><span data-stu-id="0f22e-115">For scripting development, the author of the task is specified using the [**RegistrationInfo.Author**](registrationinfo-author.md) property.</span></span>

<span data-ttu-id="0f22e-116">Per lo sviluppo in C++, l'autore dell'attività viene specificato mediante la proprietà [**IRegistrationInfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .</span><span class="sxs-lookup"><span data-stu-id="0f22e-116">For C++ development, the author of the task is specified using the [**IRegistrationInfo::Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0f22e-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f22e-117">Examples</span></span>

<span data-ttu-id="0f22e-118">Il codice XML seguente definisce l'autore di un'attività.</span><span class="sxs-lookup"><span data-stu-id="0f22e-118">The following XML defines the author of a task.</span></span>


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="0f22e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f22e-119">Requirements</span></span>



| <span data-ttu-id="0f22e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f22e-120">Requirement</span></span> | <span data-ttu-id="0f22e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0f22e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f22e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f22e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f22e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f22e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f22e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f22e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f22e-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f22e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f22e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f22e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f22e-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0f22e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0f22e-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0f22e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





