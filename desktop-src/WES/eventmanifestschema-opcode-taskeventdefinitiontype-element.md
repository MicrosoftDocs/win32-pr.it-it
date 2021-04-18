---
title: Elemento Opcode (TaskEventDefinitionType)
description: Contiene un codice operativo specifico dell'attività per un evento. Si presuppone che tutte le definizioni opcode siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- opcode element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302544"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="618b6-105">Elemento Opcode (TaskEventDefinitionType)</span><span class="sxs-lookup"><span data-stu-id="618b6-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="618b6-106">\[A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, questo elemento non è più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="618b6-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="618b6-107">Contiene un codice operativo specifico dell'attività per un evento.</span><span class="sxs-lookup"><span data-stu-id="618b6-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="618b6-108">Si presuppone che tutte le definizioni opcode siano specifiche dell'attività per l'attività che contiene le definizioni degli eventi.</span><span class="sxs-lookup"><span data-stu-id="618b6-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="618b6-109">L'elemento **OpCode** è definito dal tipo complesso [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="618b6-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="618b6-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="618b6-110">Child elements</span></span>



| <span data-ttu-id="618b6-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="618b6-111">Element</span></span>                                                   | <span data-ttu-id="618b6-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="618b6-112">Type</span></span>                                                                               | <span data-ttu-id="618b6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="618b6-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="618b6-114">**evento**</span><span class="sxs-lookup"><span data-stu-id="618b6-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="618b6-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="618b6-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="618b6-116">Evento pubblicato con un'attività.</span><span class="sxs-lookup"><span data-stu-id="618b6-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="618b6-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="618b6-117">Attributes</span></span>



| <span data-ttu-id="618b6-118">Nome</span><span class="sxs-lookup"><span data-stu-id="618b6-118">Name</span></span> | <span data-ttu-id="618b6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="618b6-119">Type</span></span>      | <span data-ttu-id="618b6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="618b6-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="618b6-121">name</span><span class="sxs-lookup"><span data-stu-id="618b6-121">name</span></span> | <span data-ttu-id="618b6-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="618b6-122">**QName**</span></span> | <span data-ttu-id="618b6-123">Nome del codice operativo specifico dell'attività.</span><span class="sxs-lookup"><span data-stu-id="618b6-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="618b6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="618b6-124">Requirements</span></span>



| <span data-ttu-id="618b6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="618b6-125">Requirement</span></span> | <span data-ttu-id="618b6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="618b6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="618b6-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="618b6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="618b6-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="618b6-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="618b6-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="618b6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="618b6-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="618b6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="618b6-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="618b6-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="618b6-132">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="618b6-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="618b6-133">**attività (DefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="618b6-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





