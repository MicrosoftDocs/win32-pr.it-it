---
title: Attachments (sendEmailType)-elemento
description: Contiene un elenco di allegati nel messaggio di posta elettronica.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Elemento Attachments Utilità di pianificazione
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742770"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="65992-104">Attachments (sendEmailType)-elemento</span><span class="sxs-lookup"><span data-stu-id="65992-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="65992-105">Contiene un elenco di allegati nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="65992-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="65992-106">L'elemento **Attachments** viene definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="65992-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="65992-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="65992-107">Parent element</span></span>



| <span data-ttu-id="65992-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="65992-108">Element</span></span>                                                                              | <span data-ttu-id="65992-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="65992-109">Derived from</span></span>                                                           | <span data-ttu-id="65992-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65992-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="65992-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="65992-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="65992-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="65992-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="65992-113">Rappresenta un'azione che invia un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="65992-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="65992-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="65992-114">Child elements</span></span>



| <span data-ttu-id="65992-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="65992-115">Element</span></span>                                                          | <span data-ttu-id="65992-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="65992-116">Type</span></span>                                                                    | <span data-ttu-id="65992-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65992-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65992-118">**File**</span><span class="sxs-lookup"><span data-stu-id="65992-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="65992-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="65992-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="65992-120">Specifica il percorso di un file inviato come allegato in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="65992-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65992-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="65992-121">Remarks</span></span>

<span data-ttu-id="65992-122">Per lo sviluppo in C++, vedere [**Proprietà Attachments di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="65992-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="65992-123">Per lo sviluppo di script, vedere [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="65992-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65992-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65992-124">Requirements</span></span>



| <span data-ttu-id="65992-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="65992-125">Requirement</span></span> | <span data-ttu-id="65992-126">Valore</span><span class="sxs-lookup"><span data-stu-id="65992-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65992-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65992-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65992-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65992-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65992-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65992-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65992-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65992-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





