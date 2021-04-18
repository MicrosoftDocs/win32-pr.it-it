---
title: Elemento Documentation (registrationInfoType)
description: Specifica qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Utilità di pianificazione elemento della documentazione
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302691"
---
# <a name="documentation-registrationinfotype-element"></a><span data-ttu-id="0aa68-104">Elemento Documentation (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="0aa68-104">Documentation (registrationInfoType) Element</span></span>

<span data-ttu-id="0aa68-105">Specifica qualsiasi documentazione aggiuntiva per l'attività.</span><span class="sxs-lookup"><span data-stu-id="0aa68-105">Specifies any additional documentation for the task.</span></span>

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="0aa68-106">L'elemento **Documentation** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa68-106">The **Documentation** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0aa68-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="0aa68-107">Parent element</span></span>



| <span data-ttu-id="0aa68-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0aa68-108">Element</span></span>                                                                           | <span data-ttu-id="0aa68-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="0aa68-109">Derived from</span></span>                                                                         | <span data-ttu-id="0aa68-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aa68-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aa68-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="0aa68-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="0aa68-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="0aa68-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="0aa68-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0aa68-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0aa68-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0aa68-114">Remarks</span></span>

<span data-ttu-id="0aa68-115">Per le applicazioni di scripting, è stata specificata una documentazione aggiuntiva sulle attività usando la proprietà [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa68-115">For scripting applications, additional task documentation is specified using the using the [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) property.</span></span>

<span data-ttu-id="0aa68-116">Per le applicazioni C++, è stata specificata una documentazione aggiuntiva sulle attività usando la proprietà [**IRegistrationInfo::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .</span><span class="sxs-lookup"><span data-stu-id="0aa68-116">For C++ applications, additional task documentation is specified using the using the [**IRegistrationInfo::Documentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa68-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aa68-117">Requirements</span></span>



| <span data-ttu-id="0aa68-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa68-118">Requirement</span></span> | <span data-ttu-id="0aa68-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0aa68-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0aa68-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aa68-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa68-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0aa68-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0aa68-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aa68-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa68-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0aa68-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0aa68-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aa68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa68-125">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0aa68-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





