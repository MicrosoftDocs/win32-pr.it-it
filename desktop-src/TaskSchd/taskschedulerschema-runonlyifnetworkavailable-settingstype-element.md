---
title: Elemento RunOnlyIfNetworkAvailable (settingsType)
description: Specifica che l'Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Utilità di pianificazione elemento RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964711"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="6c901-104">Elemento RunOnlyIfNetworkAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="6c901-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="6c901-105">Specifica che l'Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="6c901-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="6c901-106">L'elemento **RunOnlyIfNetworkAvailable** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c901-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6c901-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="6c901-107">Parent element</span></span>



| <span data-ttu-id="6c901-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c901-108">Element</span></span>                                                           | <span data-ttu-id="6c901-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="6c901-109">Derived from</span></span>                                                         | <span data-ttu-id="6c901-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c901-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c901-111">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6c901-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6c901-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="6c901-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6c901-113">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="6c901-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6c901-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c901-114">Remarks</span></span>

<span data-ttu-id="6c901-115">Per lo sviluppo in C++, vedere [**la proprietà RunOnlyIfNetworkAvailable di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="6c901-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="6c901-116">Per lo sviluppo di script, vedere [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="6c901-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c901-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="6c901-117">Examples</span></span>

<span data-ttu-id="6c901-118">Nel codice XML seguente viene definito un elemento Settings che consente l'avvio dell'attività solo se è disponibile una rete.</span><span class="sxs-lookup"><span data-stu-id="6c901-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="6c901-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c901-119">Requirements</span></span>



| <span data-ttu-id="6c901-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c901-120">Requirement</span></span> | <span data-ttu-id="6c901-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6c901-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c901-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c901-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c901-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c901-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c901-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c901-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c901-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c901-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c901-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c901-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c901-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6c901-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





