---
title: Elemento Body (showMessageType)
description: Contiene il testo da visualizzare nel corpo della finestra di messaggio.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Utilità di pianificazione elemento Body
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477470"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="1f2b9-104">Elemento Body (showMessageType)</span><span class="sxs-lookup"><span data-stu-id="1f2b9-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="1f2b9-105">Contiene il testo da visualizzare nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="1f2b9-106">L'elemento **Body** è definito dal tipo complesso [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1f2b9-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1f2b9-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1f2b9-107">Parent element</span></span>



| <span data-ttu-id="1f2b9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1f2b9-108">Element</span></span>                                                                                  | <span data-ttu-id="1f2b9-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1f2b9-109">Derived from</span></span>                                                               | <span data-ttu-id="1f2b9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f2b9-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="1f2b9-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="1f2b9-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="1f2b9-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="1f2b9-113">Rappresenta un'azione che visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="1f2b9-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1f2b9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f2b9-114">Remarks</span></span>

<span data-ttu-id="1f2b9-115">Per lo sviluppo in C++, vedere [**la proprietà MessageBody di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="1f2b9-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="1f2b9-116">Per lo sviluppo di script, vedere [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="1f2b9-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2b9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f2b9-117">Requirements</span></span>



| <span data-ttu-id="1f2b9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f2b9-118">Requirement</span></span> | <span data-ttu-id="1f2b9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1f2b9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f2b9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f2b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2b9-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f2b9-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1f2b9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f2b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2b9-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f2b9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





