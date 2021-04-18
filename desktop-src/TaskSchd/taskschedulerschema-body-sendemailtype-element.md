---
title: Elemento Body (sendEmailType)
description: Contiene il testo nel corpo del messaggio di posta elettronica.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
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
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301907"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="ab653-104">Elemento Body (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="ab653-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="ab653-105">Contiene il testo nel corpo del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ab653-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="ab653-106">L'elemento **Body** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ab653-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ab653-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ab653-107">Parent element</span></span>



| <span data-ttu-id="ab653-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ab653-108">Element</span></span>                                                                              | <span data-ttu-id="ab653-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="ab653-109">Derived from</span></span>                                                           | <span data-ttu-id="ab653-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab653-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="ab653-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="ab653-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="ab653-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="ab653-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="ab653-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ab653-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab653-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab653-114">Remarks</span></span>

<span data-ttu-id="ab653-115">Per lo sviluppo in C++, vedere [**proprietà Body di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="ab653-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="ab653-116">Per lo sviluppo di script, vedere [**EmailAction. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="ab653-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab653-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab653-117">Requirements</span></span>



| <span data-ttu-id="ab653-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab653-118">Requirement</span></span> | <span data-ttu-id="ab653-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ab653-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab653-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab653-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab653-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab653-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab653-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab653-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab653-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab653-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





