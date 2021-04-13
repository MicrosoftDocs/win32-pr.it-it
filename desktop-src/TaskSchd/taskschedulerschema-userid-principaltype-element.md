---
title: Elemento UserId (principalType)
description: Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400932"
---
# <a name="userid-principaltype-element"></a><span data-ttu-id="9441b-104">Elemento UserId (principalType)</span><span class="sxs-lookup"><span data-stu-id="9441b-104">UserId (principalType) Element</span></span>

<span data-ttu-id="9441b-105">Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="9441b-105">Specifies the user identifier required to run those tasks associated with the principal.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

<span data-ttu-id="9441b-106">L'elemento **userid** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9441b-106">The **UserId** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9441b-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9441b-107">Parent element</span></span>



| <span data-ttu-id="9441b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9441b-108">Element</span></span>                                                                  | <span data-ttu-id="9441b-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9441b-109">Derived from</span></span>                                                           | <span data-ttu-id="9441b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9441b-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9441b-111">**Principale**</span><span class="sxs-lookup"><span data-stu-id="9441b-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="9441b-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="9441b-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="9441b-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="9441b-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9441b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9441b-114">Remarks</span></span>

<span data-ttu-id="9441b-115">L'elemento **userid** e l'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) vengono utilizzati insieme per definire l'utente necessario per eseguire le attività che utilizzano questa entità.</span><span class="sxs-lookup"><span data-stu-id="9441b-115">The **UserId** element and the [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) element are used together to define the user required to run those tasks that use this principal.</span></span>

<span data-ttu-id="9441b-116">Non è possibile specificare contemporaneamente un identificatore utente e un identificatore di gruppo.</span><span class="sxs-lookup"><span data-stu-id="9441b-116">You cannot specify a user identifier and a group identifier at the same time.</span></span> <span data-ttu-id="9441b-117">Specificare l' **ID utente** o l'elemento [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) , ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="9441b-117">Specify either the **UserId** or the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element, but not both.</span></span>

<span data-ttu-id="9441b-118">Per lo sviluppo di script, l'identificatore utente viene specificato utilizzando la proprietà [**Principal. UserID**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="9441b-118">For scripting development, the user identifier is specified using the [**Principal.UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="9441b-119">Per lo sviluppo in C++, l'identificatore utente viene specificato tramite la proprietà [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="9441b-119">For C++ development, the user identifier is specified using the [**IPrincipal::UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9441b-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="9441b-120">Examples</span></span>

<span data-ttu-id="9441b-121">Il codice XML seguente definisce un principio usando un identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="9441b-121">The following XML defines a principle using a user identifier.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="9441b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9441b-122">Requirements</span></span>



| <span data-ttu-id="9441b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9441b-123">Requirement</span></span> | <span data-ttu-id="9441b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9441b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9441b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9441b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9441b-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9441b-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9441b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9441b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9441b-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9441b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9441b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9441b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9441b-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9441b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





