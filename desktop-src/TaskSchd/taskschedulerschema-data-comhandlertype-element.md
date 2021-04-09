---
title: Elemento data (comHandlerType)
description: Specifica i dati aggiuntivi associati al gestore.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Utilità di pianificazione elemento dati
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964674"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="71fe9-104">Elemento data (comHandlerType)</span><span class="sxs-lookup"><span data-stu-id="71fe9-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="71fe9-105">Specifica i dati aggiuntivi associati al gestore.</span><span class="sxs-lookup"><span data-stu-id="71fe9-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="71fe9-106">L'elemento **dati** è definito dal tipo complesso [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="71fe9-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="71fe9-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="71fe9-107">Parent element</span></span>



| <span data-ttu-id="71fe9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="71fe9-108">Element</span></span>                                                                  | <span data-ttu-id="71fe9-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="71fe9-109">Derived from</span></span>                                                             | <span data-ttu-id="71fe9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71fe9-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="71fe9-111">**Comgestore**</span><span class="sxs-lookup"><span data-stu-id="71fe9-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="71fe9-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="71fe9-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="71fe9-113">Specifica un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="71fe9-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71fe9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="71fe9-114">Remarks</span></span>

<span data-ttu-id="71fe9-115">Le applicazioni definiscono i dati del gestore usando la proprietà [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) dell'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="71fe9-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="71fe9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71fe9-116">Requirements</span></span>



| <span data-ttu-id="71fe9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71fe9-117">Requirement</span></span> | <span data-ttu-id="71fe9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="71fe9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71fe9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71fe9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71fe9-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71fe9-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71fe9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71fe9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71fe9-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71fe9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71fe9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71fe9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fe9-124">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="71fe9-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





