---
title: Tipo complesso registrationInfoType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Utilità di pianificazione di tipo complesso registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964513"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="7cca4-104">Tipo complesso registrationInfoType</span><span class="sxs-lookup"><span data-stu-id="7cca4-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="7cca4-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7cca4-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7cca4-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7cca4-106">Child elements</span></span>



| <span data-ttu-id="7cca4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7cca4-107">Element</span></span>                                                                                           | <span data-ttu-id="7cca4-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cca4-108">Type</span></span>     | <span data-ttu-id="7cca4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cca4-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cca4-110">**Autore**</span><span class="sxs-lookup"><span data-stu-id="7cca4-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="7cca4-111">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-111">string</span></span>   | <span data-ttu-id="7cca4-112">Specifica l'autore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="7cca4-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="7cca4-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="7cca4-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="7cca4-114">dateTime</span></span> | <span data-ttu-id="7cca4-115">Specifica la data e l'ora di registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="7cca4-116">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7cca4-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="7cca4-117">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-117">string</span></span>   | <span data-ttu-id="7cca4-118">Specifica la descrizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="7cca4-119">**Documentazione**</span><span class="sxs-lookup"><span data-stu-id="7cca4-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="7cca4-120">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-120">string</span></span>   | <span data-ttu-id="7cca4-121">Specifica qualsiasi documentazione aggiuntiva per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="7cca4-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7cca4-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="7cca4-123">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-123">string</span></span>   | <span data-ttu-id="7cca4-124">Specifica il descrittore di sicurezza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="7cca4-125">**Origine**</span><span class="sxs-lookup"><span data-stu-id="7cca4-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="7cca4-126">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-126">string</span></span>   | <span data-ttu-id="7cca4-127">Specifica la posizione da cui ha avuto origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-127">Specifies where the task originated from.</span></span> <span data-ttu-id="7cca4-128">Ad esempio, da un componente, un servizio, un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="7cca4-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="7cca4-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="7cca4-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="7cca4-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="7cca4-130">anyURI</span></span>   | <span data-ttu-id="7cca4-131">Specifica l'URI dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="7cca4-132">**Versione**</span><span class="sxs-lookup"><span data-stu-id="7cca4-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="7cca4-133">string</span><span class="sxs-lookup"><span data-stu-id="7cca4-133">string</span></span>   | <span data-ttu-id="7cca4-134">Specifica il numero di versione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7cca4-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="7cca4-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cca4-135">Requirements</span></span>



| <span data-ttu-id="7cca4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cca4-136">Requirement</span></span> | <span data-ttu-id="7cca4-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7cca4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cca4-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cca4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7cca4-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cca4-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cca4-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cca4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7cca4-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cca4-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cca4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cca4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cca4-143">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7cca4-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7cca4-144">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7cca4-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





