---
title: EventTrigger. ValueQueries, proprietà
description: Per la creazione di script, ottiene o imposta una raccolta di query XPath denominate. Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di sottoscrizione.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Utilità di pianificazione proprietà ValueQueries
- Utilità di pianificazione proprietà ValueQueries, oggetto EventTrigger
- Utilità di pianificazione oggetto EventTrigger, proprietà ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518508"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="24b0f-107">EventTrigger. ValueQueries, proprietà</span><span class="sxs-lookup"><span data-stu-id="24b0f-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="24b0f-108">Per la creazione di script, ottiene o imposta una raccolta di query XPath denominate.</span><span class="sxs-lookup"><span data-stu-id="24b0f-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="24b0f-109">Ogni query della raccolta viene applicata all'ultimo XML dell'evento corrispondente restituito dalla query di sottoscrizione specificata nella proprietà di [**sottoscrizione**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="24b0f-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b0f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24b0f-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="24b0f-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="24b0f-111">Property value</span></span>

<span data-ttu-id="24b0f-112">Raccolta di coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="24b0f-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="24b0f-113">Ogni coppia nome-valore nella raccolta definisce un nome univoco per il valore di una proprietà dell'evento che attiva il trigger di evento.</span><span class="sxs-lookup"><span data-stu-id="24b0f-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="24b0f-114">Il valore della proprietà dell'evento viene definito come una query di eventi XPath.</span><span class="sxs-lookup"><span data-stu-id="24b0f-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="24b0f-115">Per ulteriori informazioni sulle query di eventi XPath, vedere [Selezione eventi](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="24b0f-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="24b0f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="24b0f-116">Remarks</span></span>

<span data-ttu-id="24b0f-117">Il nome della query può essere utilizzato come variabile nelle proprietà dell'azione seguenti:</span><span class="sxs-lookup"><span data-stu-id="24b0f-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="24b0f-118">**ShowMessageAction. MessageBody**</span><span class="sxs-lookup"><span data-stu-id="24b0f-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="24b0f-119">**ShowMessageAction. title**</span><span class="sxs-lookup"><span data-stu-id="24b0f-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="24b0f-120">**ExecAction. Arguments**</span><span class="sxs-lookup"><span data-stu-id="24b0f-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="24b0f-121">**ExecAction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="24b0f-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="24b0f-122">**EmailAction. Server**</span><span class="sxs-lookup"><span data-stu-id="24b0f-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="24b0f-123">**EmailAction. Subject**</span><span class="sxs-lookup"><span data-stu-id="24b0f-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="24b0f-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="24b0f-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="24b0f-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="24b0f-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="24b0f-126">**EmailAction. Ccn**</span><span class="sxs-lookup"><span data-stu-id="24b0f-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="24b0f-127">**EmailAction. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="24b0f-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="24b0f-128">**EmailAction. from**</span><span class="sxs-lookup"><span data-stu-id="24b0f-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="24b0f-129">**EmailAction. Body**</span><span class="sxs-lookup"><span data-stu-id="24b0f-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="24b0f-130">**ComHandlerAction. Data**</span><span class="sxs-lookup"><span data-stu-id="24b0f-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="24b0f-131">Le stringhe di esempio di codice seguenti mostrano due coppie nome/valore che possono essere usate in una raccolta di valori di nome.</span><span class="sxs-lookup"><span data-stu-id="24b0f-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="24b0f-132">I valori restituiti dalle query XPath possono sostituire le variabili nella proprietà di un'azione.</span><span class="sxs-lookup"><span data-stu-id="24b0f-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="24b0f-133">Ai valori viene fatto riferimento in base al nome, con `$(user)` e `$(machine)` , nella proprietà Action.</span><span class="sxs-lookup"><span data-stu-id="24b0f-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="24b0f-134">Se, ad esempio, `$(user)` le `$(machine)` variabili e vengono utilizzate nella stringa [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , il valore delle query XPath sostituisce le variabili nella stringa.</span><span class="sxs-lookup"><span data-stu-id="24b0f-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="24b0f-135">Per ulteriori informazioni sulla scrittura di una stringa di query per determinati eventi, vedere [selezione](/previous-versions//aa385231(v=vs.85)) di eventi e [sottoscrizione degli eventi](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="24b0f-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24b0f-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b0f-136">Requirements</span></span>



| <span data-ttu-id="24b0f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b0f-137">Requirement</span></span> | <span data-ttu-id="24b0f-138">Valore</span><span class="sxs-lookup"><span data-stu-id="24b0f-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24b0f-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b0f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="24b0f-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24b0f-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="24b0f-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b0f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="24b0f-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24b0f-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24b0f-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="24b0f-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="24b0f-144"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24b0f-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24b0f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="24b0f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b0f-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b0f-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b0f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24b0f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b0f-148">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="24b0f-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="24b0f-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="24b0f-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

