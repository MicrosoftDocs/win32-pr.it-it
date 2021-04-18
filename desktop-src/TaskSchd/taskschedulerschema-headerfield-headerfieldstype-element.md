---
title: Elemento HeaderField (headerFieldsType)
description: Contiene un campo per un'intestazione in un messaggio di posta elettronica.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Utilità di pianificazione elemento HeaderField
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302690"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="eee99-104">Elemento HeaderField (headerFieldsType)</span><span class="sxs-lookup"><span data-stu-id="eee99-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="eee99-105">Contiene un campo per un'intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="eee99-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="eee99-106">L'elemento **HeaderField** è definito dal tipo complesso [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eee99-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eee99-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="eee99-107">Parent element</span></span>



| <span data-ttu-id="eee99-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="eee99-108">Element</span></span>                                                                        | <span data-ttu-id="eee99-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="eee99-109">Derived from</span></span>                                                                 | <span data-ttu-id="eee99-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee99-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee99-111">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="eee99-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="eee99-112">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="eee99-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="eee99-113">Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="eee99-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="eee99-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="eee99-114">Child elements</span></span>



| <span data-ttu-id="eee99-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="eee99-115">Element</span></span>                                                            | <span data-ttu-id="eee99-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="eee99-116">Type</span></span>                                                                    | <span data-ttu-id="eee99-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee99-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="eee99-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eee99-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="eee99-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="eee99-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="eee99-120">Specifica il nome del campo di intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="eee99-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="eee99-121">**Valore**</span><span class="sxs-lookup"><span data-stu-id="eee99-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="eee99-122">**string**</span><span class="sxs-lookup"><span data-stu-id="eee99-122">**string**</span></span>                                                              | <span data-ttu-id="eee99-123">Specifica il valore di un campo di intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="eee99-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="eee99-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="eee99-124">Remarks</span></span>

<span data-ttu-id="eee99-125">Per lo sviluppo in C++, vedere [**la proprietà HeaderFields di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="eee99-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="eee99-126">Per lo sviluppo di script, vedere [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="eee99-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eee99-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eee99-127">Requirements</span></span>



| <span data-ttu-id="eee99-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee99-128">Requirement</span></span> | <span data-ttu-id="eee99-129">Valore</span><span class="sxs-lookup"><span data-stu-id="eee99-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eee99-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eee99-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eee99-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eee99-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eee99-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eee99-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eee99-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eee99-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





