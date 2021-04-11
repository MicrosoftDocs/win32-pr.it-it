---
title: Elemento ReplyTo (sendEmailType)
description: Contiene gli indirizzi di posta elettronica a cui viene risposto nel messaggio di posta elettronica.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo-elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121555"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="99458-104">Elemento ReplyTo (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="99458-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="99458-105">Contiene gli indirizzi di posta elettronica a cui viene risposto nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="99458-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="99458-106">L'elemento **ReplyTo** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="99458-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="99458-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="99458-107">Parent element</span></span>



| <span data-ttu-id="99458-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="99458-108">Element</span></span>                                                                              | <span data-ttu-id="99458-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="99458-109">Derived from</span></span>                                                           | <span data-ttu-id="99458-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99458-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="99458-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="99458-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="99458-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="99458-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="99458-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="99458-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="99458-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="99458-114">Remarks</span></span>

<span data-ttu-id="99458-115">Per lo sviluppo in C++, vedere [**la proprietà ReplyTo di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="99458-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="99458-116">Per lo sviluppo di script, vedere [**EmailAction. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="99458-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99458-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99458-117">Requirements</span></span>



| <span data-ttu-id="99458-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99458-118">Requirement</span></span> | <span data-ttu-id="99458-119">Valore</span><span class="sxs-lookup"><span data-stu-id="99458-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99458-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99458-120">Minimum supported client</span></span><br/> | <span data-ttu-id="99458-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99458-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99458-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99458-122">Minimum supported server</span></span><br/> | <span data-ttu-id="99458-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99458-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





