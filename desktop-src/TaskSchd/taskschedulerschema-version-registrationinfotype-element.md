---
title: Version (registrationInfoType)-elemento
description: Specifica il numero di versione dell'attività.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento version Utilità di pianificazione
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301144"
---
# <a name="version-registrationinfotype-element"></a><span data-ttu-id="d696c-104">Version (registrationInfoType)-elemento</span><span class="sxs-lookup"><span data-stu-id="d696c-104">Version (registrationInfoType) Element</span></span>

<span data-ttu-id="d696c-105">Specifica il numero di versione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="d696c-105">Specifies the version number of the task.</span></span>

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="d696c-106">L'elemento **Version** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d696c-106">The **Version** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d696c-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d696c-107">Parent element</span></span>



| <span data-ttu-id="d696c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d696c-108">Element</span></span>                                                                           | <span data-ttu-id="d696c-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="d696c-109">Derived from</span></span>                                                                         | <span data-ttu-id="d696c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d696c-110">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d696c-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="d696c-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="d696c-112">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="d696c-112">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="d696c-113">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="d696c-113">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d696c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d696c-114">Remarks</span></span>

<span data-ttu-id="d696c-115">Per lo sviluppo di script, la versione di un'attività viene specificata utilizzando la proprietà [**RegistrationInfo. Version**](registrationinfo-version.md) .</span><span class="sxs-lookup"><span data-stu-id="d696c-115">For scripting development, the version of a task is specified using [**RegistrationInfo.Version**](registrationinfo-version.md) property.</span></span>

<span data-ttu-id="d696c-116">Per lo sviluppo in C++, la versione di un'attività viene specificata utilizzando la proprietà [**IRegistrationInfo:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .</span><span class="sxs-lookup"><span data-stu-id="d696c-116">For C++ development, the version of a task is specified using [**IRegistrationInfo::Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) property.</span></span>

## <a name="examples"></a><span data-ttu-id="d696c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d696c-117">Examples</span></span>

<span data-ttu-id="d696c-118">Il codice XML seguente definisce la versione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="d696c-118">The following XML defines the version of a task.</span></span>


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a><span data-ttu-id="d696c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d696c-119">Requirements</span></span>



| <span data-ttu-id="d696c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d696c-120">Requirement</span></span> | <span data-ttu-id="d696c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d696c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d696c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d696c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d696c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d696c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d696c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d696c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d696c-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d696c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d696c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d696c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d696c-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d696c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d696c-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d696c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





