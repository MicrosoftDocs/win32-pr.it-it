---
title: Elemento HeaderFields (sendEmailType)
description: Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Utilità di pianificazione elemento HeaderFields
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518190"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="4da20-104">Elemento HeaderFields (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="4da20-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="4da20-105">Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4da20-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="4da20-106">L'elemento **HeaderFields** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4da20-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4da20-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4da20-107">Parent element</span></span>



| <span data-ttu-id="4da20-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4da20-108">Element</span></span>                                                                              | <span data-ttu-id="4da20-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="4da20-109">Derived from</span></span>                                                           | <span data-ttu-id="4da20-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4da20-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4da20-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="4da20-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="4da20-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="4da20-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="4da20-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4da20-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4da20-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4da20-114">Child elements</span></span>



| <span data-ttu-id="4da20-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="4da20-115">Element</span></span>                                                                         | <span data-ttu-id="4da20-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4da20-116">Type</span></span>                                                                       | <span data-ttu-id="4da20-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4da20-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="4da20-118">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="4da20-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="4da20-119">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="4da20-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="4da20-120">Contiene un campo per un'intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4da20-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="4da20-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="4da20-121">Remarks</span></span>

<span data-ttu-id="4da20-122">Per lo sviluppo in C++, vedere [**la proprietà HeaderFields di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="4da20-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="4da20-123">Per lo sviluppo di script, vedere [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="4da20-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4da20-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4da20-124">Requirements</span></span>



| <span data-ttu-id="4da20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da20-125">Requirement</span></span> | <span data-ttu-id="4da20-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4da20-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4da20-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4da20-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4da20-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4da20-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4da20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4da20-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4da20-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





