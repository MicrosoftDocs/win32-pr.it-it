---
title: Elemento URI (registrationInfoType)
description: Specifica l'URI dell'attività.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Utilità di pianificazione elemento URI
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743751"
---
# <a name="uri-registrationinfotype-element"></a><span data-ttu-id="5bcdc-104">Elemento URI (registrationInfoType)</span><span class="sxs-lookup"><span data-stu-id="5bcdc-104">URI (registrationInfoType) Element</span></span>

<span data-ttu-id="5bcdc-105">Specifica l'URI dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-105">Specifies the URI of the task.</span></span> <span data-ttu-id="5bcdc-106">Questo elemento viene utilizzato per specificare il percorso in cui l'attività registrata viene posizionata nella gerarchia delle cartelle delle attività.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-106">This element is used to specify where the registered task is placed in the task folder hierarchy.</span></span>

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

<span data-ttu-id="5bcdc-107">L'elemento **URI** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5bcdc-107">The **URI** element is defined by the [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5bcdc-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5bcdc-108">Parent element</span></span>



| <span data-ttu-id="5bcdc-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="5bcdc-109">Element</span></span>                                                                           | <span data-ttu-id="5bcdc-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="5bcdc-110">Derived from</span></span>                                                                         | <span data-ttu-id="5bcdc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bcdc-111">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bcdc-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="5bcdc-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="5bcdc-113">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="5bcdc-113">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="5bcdc-114">Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-114">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5bcdc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bcdc-115">Remarks</span></span>

<span data-ttu-id="5bcdc-116">Per lo sviluppo di script, l'URI dell'attività viene specificato mediante la proprietà [**RegistrationInfo. Uri**](registrationinfo-uri.md) .</span><span class="sxs-lookup"><span data-stu-id="5bcdc-116">For scripting development, the URI of the task is specified using the [**RegistrationInfo.URI**](registrationinfo-uri.md) property.</span></span>

<span data-ttu-id="5bcdc-117">Per lo sviluppo in C++, l'URI dell'attività viene specificato mediante la proprietà [**IRegistrationInfo:: URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) .</span><span class="sxs-lookup"><span data-stu-id="5bcdc-117">For C++ development, the URI of the task is specified using the [**IRegistrationInfo::URI**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bcdc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bcdc-118">Requirements</span></span>



| <span data-ttu-id="5bcdc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bcdc-119">Requirement</span></span> | <span data-ttu-id="5bcdc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5bcdc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bcdc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bcdc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5bcdc-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bcdc-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5bcdc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bcdc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5bcdc-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bcdc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bcdc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bcdc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bcdc-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5bcdc-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5bcdc-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5bcdc-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





