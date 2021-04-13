---
title: Elemento Source (registrationInfoType)
description: Specifica la posizione da cui ha avuto origine l'attività. Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento Source Utilità di pianificazione
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400342"
---
# <a name="source-registrationinfotype-element"></a><span data-ttu-id="1675d-105">Elemento Source (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="1675d-105">Source (registrationInfoType) Element</span></span>

<span data-ttu-id="1675d-106">Specifica la posizione da cui ha avuto origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="1675d-106">Specifies where the task originated from.</span></span> <span data-ttu-id="1675d-107">Ad esempio, da un componente, da un servizio, da un'applicazione o da un utente.</span><span class="sxs-lookup"><span data-stu-id="1675d-107">For example, from a component, a service, an application, or a user.</span></span>

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="1675d-108">L'elemento di **origine** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1675d-108">The **Source** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1675d-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1675d-109">Parent element</span></span>



| <span data-ttu-id="1675d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="1675d-110">Element</span></span>                                                                           | <span data-ttu-id="1675d-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1675d-111">Derived from</span></span>                                                                         | <span data-ttu-id="1675d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1675d-112">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1675d-113">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="1675d-113">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="1675d-114">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="1675d-114">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="1675d-115">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1675d-115">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1675d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1675d-116">Remarks</span></span>

<span data-ttu-id="1675d-117">Per lo sviluppo di script, l'origine di un'attività viene specificata utilizzando la proprietà [**RegistrationInfo. Source**](registrationinfo-source.md) .</span><span class="sxs-lookup"><span data-stu-id="1675d-117">For scripting development, the source of a task is specified using the [**RegistrationInfo.Source**](registrationinfo-source.md) property.</span></span>

<span data-ttu-id="1675d-118">Per lo sviluppo in C++, l'origine di un'attività viene specificata tramite la proprietà [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .</span><span class="sxs-lookup"><span data-stu-id="1675d-118">For C++ development, the source of a task is specified using the [**IRegistrationInfo::Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1675d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1675d-119">Requirements</span></span>



| <span data-ttu-id="1675d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1675d-120">Requirement</span></span> | <span data-ttu-id="1675d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1675d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1675d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1675d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1675d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1675d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1675d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1675d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1675d-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1675d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1675d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1675d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1675d-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1675d-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1675d-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1675d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





