---
title: Elemento UserId (sessionStateChangeTriggerType)
description: Contiene l'utente per la sessione di Terminal Server. Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- Elemento UserId Utilità di pianificazione
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518586"
---
# <a name="userid-sessionstatechangetriggertype-element"></a><span data-ttu-id="66333-105">Elemento UserId (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="66333-105">UserId (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="66333-106">Contiene l'utente per la sessione di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="66333-106">Contains the user for the Terminal Server session.</span></span> <span data-ttu-id="66333-107">Quando viene rilevata una modifica dello stato della sessione per questo utente, viene avviata un'attività.</span><span class="sxs-lookup"><span data-stu-id="66333-107">When a session state change is detected for this user, a task is started.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="66333-108">L'elemento **userid** è definito dal tipo complesso [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="66333-108">The **UserId** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="66333-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="66333-109">Parent element</span></span>



| <span data-ttu-id="66333-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="66333-110">Element</span></span>                       | <span data-ttu-id="66333-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="66333-111">Derived from</span></span>                                                                                           | <span data-ttu-id="66333-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66333-112">Description</span></span>                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66333-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="66333-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="66333-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="66333-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="66333-115">Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="66333-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="66333-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="66333-116">Remarks</span></span>

<span data-ttu-id="66333-117">Per lo sviluppo in C++, vedere [**userid Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span><span class="sxs-lookup"><span data-stu-id="66333-117">For C++ development, see [**UserId Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).</span></span>

<span data-ttu-id="66333-118">Per lo sviluppo di script, vedere [**SessionStateChangeTrigger. UserID**](sessionstatechangetrigger-userid.md).</span><span class="sxs-lookup"><span data-stu-id="66333-118">For script development, see [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66333-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66333-119">Requirements</span></span>



| <span data-ttu-id="66333-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="66333-120">Requirement</span></span> | <span data-ttu-id="66333-121">Valore</span><span class="sxs-lookup"><span data-stu-id="66333-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66333-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66333-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66333-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66333-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66333-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66333-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66333-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66333-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





