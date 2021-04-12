---
title: Elemento Subject (sendEmailType)
description: Contiene l'oggetto del messaggio di posta elettronica.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Utilità di pianificazione elemento oggetto
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519118"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="d30d5-104">Elemento Subject (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="d30d5-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="d30d5-105">Contiene l'oggetto del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="d30d5-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="d30d5-106">L'elemento **Subject** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d30d5-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d30d5-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d30d5-107">Parent element</span></span>



| <span data-ttu-id="d30d5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="d30d5-108">Element</span></span>                                                                              | <span data-ttu-id="d30d5-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="d30d5-109">Derived from</span></span>                                                           | <span data-ttu-id="d30d5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30d5-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d30d5-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="d30d5-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d30d5-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="d30d5-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d30d5-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="d30d5-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d30d5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d30d5-114">Remarks</span></span>

<span data-ttu-id="d30d5-115">Per lo sviluppo in C++, vedere [**proprietà Subject di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="d30d5-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="d30d5-116">Per lo sviluppo di script, vedere [**EmailAction. Subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="d30d5-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d30d5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d30d5-117">Requirements</span></span>



| <span data-ttu-id="d30d5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d30d5-118">Requirement</span></span> | <span data-ttu-id="d30d5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d30d5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d30d5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d30d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d30d5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d30d5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d30d5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d30d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d30d5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d30d5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





