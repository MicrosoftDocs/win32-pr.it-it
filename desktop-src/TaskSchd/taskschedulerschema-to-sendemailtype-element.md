---
title: Elemento to (sendEmailType)
description: Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- All'elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301145"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="ccf43-104">Elemento to (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="ccf43-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="ccf43-105">Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ccf43-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="ccf43-106">L'elemento **to** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf43-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ccf43-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ccf43-107">Parent element</span></span>



| <span data-ttu-id="ccf43-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ccf43-108">Element</span></span>                                                                              | <span data-ttu-id="ccf43-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="ccf43-109">Derived from</span></span>                                                           | <span data-ttu-id="ccf43-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf43-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="ccf43-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="ccf43-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="ccf43-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="ccf43-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="ccf43-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ccf43-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ccf43-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccf43-114">Remarks</span></span>

<span data-ttu-id="ccf43-115">Per lo sviluppo in C++, vedere [**to property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="ccf43-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="ccf43-116">Per lo sviluppo di script, vedere [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="ccf43-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf43-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf43-117">Requirements</span></span>



| <span data-ttu-id="ccf43-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf43-118">Requirement</span></span> | <span data-ttu-id="ccf43-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf43-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ccf43-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf43-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf43-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccf43-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ccf43-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf43-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf43-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccf43-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





