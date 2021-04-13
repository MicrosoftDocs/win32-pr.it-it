---
title: Elemento ShowMessage (actionGroup)
description: Rappresenta un'azione che visualizza una finestra di messaggio.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Utilità di pianificazione elemento ShowMessage
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340493"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="59a51-104">Elemento ShowMessage (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="59a51-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="59a51-105">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="59a51-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="59a51-106">L'elemento **ShowMessage** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="59a51-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="59a51-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="59a51-107">Parent element</span></span>



| <span data-ttu-id="59a51-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="59a51-108">Element</span></span>                                                                    | <span data-ttu-id="59a51-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="59a51-109">Derived from</span></span>                                                       | <span data-ttu-id="59a51-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a51-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="59a51-111">**Azioni (taskType)**</span><span class="sxs-lookup"><span data-stu-id="59a51-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="59a51-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="59a51-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="59a51-113">Contiene le azioni eseguite dall'attività.</span><span class="sxs-lookup"><span data-stu-id="59a51-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="59a51-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="59a51-114">Child elements</span></span>



| <span data-ttu-id="59a51-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="59a51-115">Element</span></span>                                                            | <span data-ttu-id="59a51-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="59a51-116">Type</span></span>           | <span data-ttu-id="59a51-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59a51-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="59a51-118">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="59a51-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="59a51-119">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="59a51-119">nonEmptyString</span></span> | <span data-ttu-id="59a51-120">Specifica il testo da visualizzare nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="59a51-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="59a51-121">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="59a51-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="59a51-122">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="59a51-122">nonEmptyString</span></span> | <span data-ttu-id="59a51-123">Specifica il titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="59a51-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="59a51-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="59a51-124">Remarks</span></span>

<span data-ttu-id="59a51-125">Per lo sviluppo di script, viene specificata un'azione MessageBox utilizzando l'oggetto [**ShowMessageAction**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="59a51-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="59a51-126">Per lo sviluppo in C++, un'azione della finestra di messaggio viene specificata tramite l'interfaccia [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .</span><span class="sxs-lookup"><span data-stu-id="59a51-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="59a51-127">**Windows 8 e Windows Server 2012:** Questo elemento è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="59a51-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="59a51-128">È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.</span><span class="sxs-lookup"><span data-stu-id="59a51-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="59a51-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="59a51-129">Examples</span></span>

<span data-ttu-id="59a51-130">Per un esempio completo del codice XML per un'attività che usa un'azione MessageBox, vedere [esempio di finestra di messaggio (XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59a51-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="59a51-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59a51-131">Requirements</span></span>



| <span data-ttu-id="59a51-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a51-132">Requirement</span></span> | <span data-ttu-id="59a51-133">Valore</span><span class="sxs-lookup"><span data-stu-id="59a51-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59a51-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59a51-134">Minimum supported client</span></span><br/> | <span data-ttu-id="59a51-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59a51-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59a51-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59a51-136">Minimum supported server</span></span><br/> | <span data-ttu-id="59a51-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59a51-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="59a51-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="59a51-138">End of client support</span></span><br/>    | <span data-ttu-id="59a51-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59a51-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="59a51-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="59a51-140">End of server support</span></span><br/>    | <span data-ttu-id="59a51-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59a51-141">Windows Server 2008 R2</span></span><br/>                    |



 

