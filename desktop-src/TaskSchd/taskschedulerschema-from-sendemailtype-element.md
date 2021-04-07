---
title: Elemento from (sendEmailType)
description: Contiene l'indirizzo di posta elettronica del mittente del messaggio di posta elettronica.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Da elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048150"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="4330a-104">Elemento from (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="4330a-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="4330a-105">Contiene l'indirizzo di posta elettronica del mittente del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4330a-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="4330a-106">L'elemento **from** viene definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4330a-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4330a-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4330a-107">Parent element</span></span>



| <span data-ttu-id="4330a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4330a-108">Element</span></span>                                                                              | <span data-ttu-id="4330a-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4330a-109">Derived from</span></span>                                                           | <span data-ttu-id="4330a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4330a-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4330a-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="4330a-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="4330a-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="4330a-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="4330a-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4330a-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4330a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4330a-114">Remarks</span></span>

<span data-ttu-id="4330a-115">Per lo sviluppo in C++, vedere la [**Proprietà from di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="4330a-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="4330a-116">Per lo sviluppo di script, vedere [**EmailAction. from**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="4330a-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4330a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4330a-117">Requirements</span></span>



| <span data-ttu-id="4330a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4330a-118">Requirement</span></span> | <span data-ttu-id="4330a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4330a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4330a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4330a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4330a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4330a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4330a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4330a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4330a-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4330a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





