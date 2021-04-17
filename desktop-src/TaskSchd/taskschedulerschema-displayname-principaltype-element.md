---
title: Elemento DisplayName (principalType)
description: Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Utilità di pianificazione
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519134"
---
# <a name="displayname-principaltype-element"></a><span data-ttu-id="139ce-104">Elemento DisplayName (principalType)</span><span class="sxs-lookup"><span data-stu-id="139ce-104">DisplayName (principalType) Element</span></span>

<span data-ttu-id="139ce-105">Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="139ce-105">Specifies the name of the principal that is displayed in the Task Scheduler UI.</span></span>

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

<span data-ttu-id="139ce-106">L'elemento **DisplayName** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="139ce-106">The **DisplayName** element is defined by the [**principalType**](taskschedulerschema-principaltype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="139ce-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="139ce-107">Parent element</span></span>



| <span data-ttu-id="139ce-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="139ce-108">Element</span></span>                                                                  | <span data-ttu-id="139ce-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="139ce-109">Derived from</span></span>                                                           | <span data-ttu-id="139ce-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="139ce-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="139ce-111">**Principale**</span><span class="sxs-lookup"><span data-stu-id="139ce-111">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="139ce-112">**principalType**</span><span class="sxs-lookup"><span data-stu-id="139ce-112">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="139ce-113">Specifica le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="139ce-113">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="139ce-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="139ce-114">Remarks</span></span>

<span data-ttu-id="139ce-115">Per lo sviluppo di script, il nome visualizzato dell'entità viene specificato utilizzando la proprietà [**Principal. DisplayName**](principal-displayname.md) .</span><span class="sxs-lookup"><span data-stu-id="139ce-115">For scripting development, the display name of the principal is specified using the [**Principal.DisplayName**](principal-displayname.md) property.</span></span>

<span data-ttu-id="139ce-116">Per lo sviluppo in C++, il nome visualizzato dell'entità viene specificato tramite la proprietà [**IPrincipal::D**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) la proprietà.</span><span class="sxs-lookup"><span data-stu-id="139ce-116">For C++ development, the display name of the principal is specified using the [**IPrincipal::DisplayName**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) property.</span></span>

## <a name="examples"></a><span data-ttu-id="139ce-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="139ce-117">Examples</span></span>

<span data-ttu-id="139ce-118">Nel codice XML seguente viene definito un oggetto utilizzando un identificatore di gruppo e un nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="139ce-118">The following XML defines a using a group identifier and a display name.</span></span>


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



<span data-ttu-id="139ce-119">Il codice XML seguente definisce un'entità usando un identificatore utente e un nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="139ce-119">The following XML defines a principal using a user identifier and a display name.</span></span>


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a><span data-ttu-id="139ce-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="139ce-120">Requirements</span></span>



| <span data-ttu-id="139ce-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="139ce-121">Requirement</span></span> | <span data-ttu-id="139ce-122">Valore</span><span class="sxs-lookup"><span data-stu-id="139ce-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="139ce-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="139ce-123">Minimum supported client</span></span><br/> | <span data-ttu-id="139ce-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="139ce-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="139ce-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="139ce-125">Minimum supported server</span></span><br/> | <span data-ttu-id="139ce-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="139ce-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="139ce-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="139ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="139ce-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="139ce-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





