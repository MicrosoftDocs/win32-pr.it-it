---
title: Elemento StateChange (sessionStateChangeTriggerType)
description: Contiene il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- Utilità di pianificazione elemento StateChange
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121550"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a><span data-ttu-id="a4fb1-104">Elemento StateChange (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="a4fb1-104">StateChange (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="a4fb1-105">Contiene il tipo di modifica della sessione di Terminal Server che attiverà l'avvio di un'attività.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-105">Contains the kind of Terminal Server session change that would trigger a task launch.</span></span>

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

<span data-ttu-id="a4fb1-106">L'elemento **StateChange** è definito dal tipo complesso [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a4fb1-106">The **StateChange** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a4fb1-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="a4fb1-107">Parent element</span></span>



| <span data-ttu-id="a4fb1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a4fb1-108">Element</span></span>                       | <span data-ttu-id="a4fb1-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="a4fb1-109">Derived from</span></span>                                                                                           | <span data-ttu-id="a4fb1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4fb1-110">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4fb1-111">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="a4fb1-111">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="a4fb1-112">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="a4fb1-112">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="a4fb1-113">Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a4fb1-113">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a4fb1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4fb1-114">Remarks</span></span>

<span data-ttu-id="a4fb1-115">Per lo sviluppo in C++, vedere [**la proprietà StateChange di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span><span class="sxs-lookup"><span data-stu-id="a4fb1-115">For C++ development, see [**StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).</span></span>

<span data-ttu-id="a4fb1-116">Per lo sviluppo di script, vedere [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md).</span><span class="sxs-lookup"><span data-stu-id="a4fb1-116">For script development, see [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4fb1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4fb1-117">Requirements</span></span>



| <span data-ttu-id="a4fb1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4fb1-118">Requirement</span></span> | <span data-ttu-id="a4fb1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a4fb1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4fb1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4fb1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4fb1-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4fb1-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4fb1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4fb1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4fb1-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4fb1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





