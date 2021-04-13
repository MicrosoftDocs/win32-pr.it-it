---
title: Elemento file (attachmentsType)
description: Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Utilità di pianificazione elemento file
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400476"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="85ab5-104">Elemento file (attachmentsType)</span><span class="sxs-lookup"><span data-stu-id="85ab5-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="85ab5-105">Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="85ab5-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="85ab5-106">L'elemento **file** è definito dal tipo complesso [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="85ab5-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="85ab5-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="85ab5-107">Parent element</span></span>



| <span data-ttu-id="85ab5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="85ab5-108">Element</span></span>                                                                                      | <span data-ttu-id="85ab5-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="85ab5-109">Derived from</span></span>                                                               | <span data-ttu-id="85ab5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ab5-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="85ab5-111">**Allegati (sendEmailType)**</span><span class="sxs-lookup"><span data-stu-id="85ab5-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="85ab5-112">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="85ab5-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="85ab5-113">Contiene un elenco di allegati nel messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="85ab5-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="85ab5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ab5-114">Remarks</span></span>

<span data-ttu-id="85ab5-115">Per lo sviluppo in C++, vedere [**Proprietà Attachments di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="85ab5-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="85ab5-116">Per lo sviluppo di script, vedere [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="85ab5-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ab5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85ab5-117">Requirements</span></span>



| <span data-ttu-id="85ab5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ab5-118">Requirement</span></span> | <span data-ttu-id="85ab5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="85ab5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85ab5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ab5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85ab5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85ab5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85ab5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ab5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85ab5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85ab5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





