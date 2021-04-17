---
title: Elemento CC (sendEmailType)
description: Contiene gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Utilità di pianificazione elemento CC
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477794"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="44775-104">Elemento CC (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="44775-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="44775-105">Contiene gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="44775-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="44775-106">L'elemento **CC** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="44775-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="44775-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="44775-107">Parent element</span></span>



| <span data-ttu-id="44775-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="44775-108">Element</span></span>                                                                              | <span data-ttu-id="44775-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="44775-109">Derived from</span></span>                                                           | <span data-ttu-id="44775-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44775-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="44775-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="44775-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="44775-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="44775-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="44775-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="44775-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44775-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="44775-114">Remarks</span></span>

<span data-ttu-id="44775-115">Per lo sviluppo in C++, vedere [**la proprietà CC di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="44775-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="44775-116">Per lo sviluppo di script, vedere [**EmailAction.CC**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="44775-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44775-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44775-117">Requirements</span></span>



| <span data-ttu-id="44775-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="44775-118">Requirement</span></span> | <span data-ttu-id="44775-119">Valore</span><span class="sxs-lookup"><span data-stu-id="44775-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44775-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44775-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44775-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44775-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44775-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44775-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44775-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44775-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





