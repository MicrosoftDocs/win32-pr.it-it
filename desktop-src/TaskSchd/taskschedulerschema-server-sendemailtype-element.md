---
title: Elemento server (sendEmailType)
description: Contiene il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Utilità di pianificazione elemento server
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400343"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="a700d-104">Elemento server (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="a700d-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="a700d-105">Contiene il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a700d-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="a700d-106">L'elemento **Server** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a700d-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a700d-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="a700d-107">Parent element</span></span>



| <span data-ttu-id="a700d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a700d-108">Element</span></span>                                                                              | <span data-ttu-id="a700d-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="a700d-109">Derived from</span></span>                                                           | <span data-ttu-id="a700d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a700d-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a700d-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="a700d-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="a700d-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="a700d-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="a700d-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a700d-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a700d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a700d-114">Remarks</span></span>

<span data-ttu-id="a700d-115">Per lo sviluppo in C++, vedere [**Proprietà server di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="a700d-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="a700d-116">Per lo sviluppo di script, vedere [**EmailAction. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="a700d-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a700d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a700d-117">Requirements</span></span>



| <span data-ttu-id="a700d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a700d-118">Requirement</span></span> | <span data-ttu-id="a700d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a700d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a700d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a700d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a700d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a700d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a700d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a700d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a700d-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a700d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





