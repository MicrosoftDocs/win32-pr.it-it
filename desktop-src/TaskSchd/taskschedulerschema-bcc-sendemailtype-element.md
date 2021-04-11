---
title: Elemento Ccn (sendEmailType)
description: Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Utilità di pianificazione elemento Ccn
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120218"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="9d330-104">Elemento Ccn (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="9d330-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="9d330-105">Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="9d330-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="9d330-106">L'elemento **Ccn** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9d330-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9d330-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9d330-107">Parent element</span></span>



| <span data-ttu-id="9d330-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9d330-108">Element</span></span>                                                                              | <span data-ttu-id="9d330-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9d330-109">Derived from</span></span>                                                           | <span data-ttu-id="9d330-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d330-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="9d330-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="9d330-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="9d330-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="9d330-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="9d330-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="9d330-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9d330-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d330-114">Remarks</span></span>

<span data-ttu-id="9d330-115">Per lo sviluppo in C++, vedere [**proprietà Ccn di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="9d330-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="9d330-116">Per lo sviluppo di script, vedere [**EmailAction. Ccn**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="9d330-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d330-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d330-117">Requirements</span></span>



| <span data-ttu-id="9d330-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d330-118">Requirement</span></span> | <span data-ttu-id="9d330-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9d330-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d330-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d330-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d330-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d330-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d330-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d330-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d330-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d330-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





