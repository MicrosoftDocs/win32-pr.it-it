---
title: Tipo complesso RenderingInfoType
description: Definisce i messaggi di cui è stato eseguito il rendering per l'evento.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Log eventi di tipo complesso RenderingInfoType
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478791"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="f04a6-104">Tipo complesso RenderingInfoType</span><span class="sxs-lookup"><span data-stu-id="f04a6-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="f04a6-105">Definisce i messaggi di cui è stato eseguito il rendering per l'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f04a6-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f04a6-106">Child elements</span></span>



| <span data-ttu-id="f04a6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f04a6-107">Element</span></span>                                                             | <span data-ttu-id="f04a6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f04a6-108">Type</span></span>   | <span data-ttu-id="f04a6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f04a6-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="f04a6-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="f04a6-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="f04a6-111">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-111">string</span></span> | <span data-ttu-id="f04a6-112">Stringa del messaggio di cui è stato eseguito il rendering del canale specificato nell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="f04a6-113">**Parola chiave**</span><span class="sxs-lookup"><span data-stu-id="f04a6-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="f04a6-114">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-114">string</span></span> | <span data-ttu-id="f04a6-115">Stringa del messaggio di cui è stato eseguito il rendering di una parola chiave specificata nell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="f04a6-116">**Parole chiave**</span><span class="sxs-lookup"><span data-stu-id="f04a6-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="f04a6-117">Elenco di parole chiave sottoposte a rendering.</span><span class="sxs-lookup"><span data-stu-id="f04a6-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="f04a6-118">**Livello**</span><span class="sxs-lookup"><span data-stu-id="f04a6-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="f04a6-119">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-119">string</span></span> | <span data-ttu-id="f04a6-120">Stringa del messaggio di cui è stato eseguito il rendering del livello specificato nell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="f04a6-121">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="f04a6-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="f04a6-122">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-122">string</span></span> | <span data-ttu-id="f04a6-123">Stringa del messaggio di cui è stato eseguito il rendering dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="f04a6-124">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="f04a6-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="f04a6-125">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-125">string</span></span> | <span data-ttu-id="f04a6-126">Stringa del messaggio di cui è stato eseguito il rendering del codice operativo specificato nell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="f04a6-127">**Provider**</span><span class="sxs-lookup"><span data-stu-id="f04a6-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="f04a6-128">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-128">string</span></span> | <span data-ttu-id="f04a6-129">Stringa di messaggio di cui è stato eseguito il rendering per il provider.</span><span class="sxs-lookup"><span data-stu-id="f04a6-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="f04a6-130">**Attività**</span><span class="sxs-lookup"><span data-stu-id="f04a6-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="f04a6-131">string</span><span class="sxs-lookup"><span data-stu-id="f04a6-131">string</span></span> | <span data-ttu-id="f04a6-132">Stringa del messaggio di cui è stato eseguito il rendering dell'attività specificata nell'evento.</span><span class="sxs-lookup"><span data-stu-id="f04a6-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="f04a6-133">Attributi</span><span class="sxs-lookup"><span data-stu-id="f04a6-133">Attributes</span></span>



| <span data-ttu-id="f04a6-134">Nome</span><span class="sxs-lookup"><span data-stu-id="f04a6-134">Name</span></span>    | <span data-ttu-id="f04a6-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="f04a6-135">Type</span></span>     | <span data-ttu-id="f04a6-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f04a6-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04a6-137">culture</span><span class="sxs-lookup"><span data-stu-id="f04a6-137">Culture</span></span> | <span data-ttu-id="f04a6-138">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="f04a6-138">language</span></span> | <span data-ttu-id="f04a6-139">Nome della lingua (ad esempio, en-US) che identifica le impostazioni locali utilizzate per il rendering delle stringhe di messaggio.</span><span class="sxs-lookup"><span data-stu-id="f04a6-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f04a6-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="f04a6-140">Remarks</span></span>

<span data-ttu-id="f04a6-141">Questa sezione contiene solo gli eventi che sono stati raccolti tramite il servizio [raccolta eventi di Windows](/windows/desktop/WEC/windows-event-collector) .</span><span class="sxs-lookup"><span data-stu-id="f04a6-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="f04a6-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f04a6-142">Requirements</span></span>



| <span data-ttu-id="f04a6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f04a6-143">Requirement</span></span> | <span data-ttu-id="f04a6-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f04a6-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f04a6-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f04a6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f04a6-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f04a6-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f04a6-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f04a6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f04a6-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f04a6-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

