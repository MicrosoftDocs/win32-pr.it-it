---
title: Elemento ClassID (comHandlerType)
description: Specifica l'identificatore della classe del gestore.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- Elemento ClassID Utilità di pianificazione
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479240"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="e7a96-104">Elemento ClassID (comHandlerType)</span><span class="sxs-lookup"><span data-stu-id="e7a96-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="e7a96-105">Specifica l'identificatore della classe del gestore.</span><span class="sxs-lookup"><span data-stu-id="e7a96-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="e7a96-106">L'elemento **ClassID** è definito dal tipo complesso [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e7a96-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e7a96-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e7a96-107">Parent element</span></span>



| <span data-ttu-id="e7a96-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7a96-108">Element</span></span>                                                                  | <span data-ttu-id="e7a96-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e7a96-109">Derived from</span></span>                                                             | <span data-ttu-id="e7a96-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7a96-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="e7a96-111">**Comgestore**</span><span class="sxs-lookup"><span data-stu-id="e7a96-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="e7a96-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="e7a96-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="e7a96-113">Specifica un'azione che attiva un gestore.</span><span class="sxs-lookup"><span data-stu-id="e7a96-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7a96-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7a96-114">Remarks</span></span>

<span data-ttu-id="e7a96-115">Le applicazioni definiscono l'identificatore di classe usando la proprietà [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) dell'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="e7a96-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a96-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7a96-116">Requirements</span></span>



| <span data-ttu-id="e7a96-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a96-117">Requirement</span></span> | <span data-ttu-id="e7a96-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a96-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7a96-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7a96-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a96-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7a96-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7a96-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7a96-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a96-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7a96-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7a96-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7a96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a96-124">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e7a96-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





