---
title: Tipo complesso TaskEventDefinitionType
description: Definisce un evento specifico dell'attività che il provider è in grado di registrare. | Tipo complesso TaskEventDefinitionType
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- Log eventi di tipo complesso TaskEventDefinitionType
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321706"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="28b07-105">Tipo complesso TaskEventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="28b07-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="28b07-106">\[A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, il tipo complesso TaskEventDefinitionType non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="28b07-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="28b07-107">Usare invece i codici operativi specifici delle attività per fornire la stessa funzionalità.\]</span><span class="sxs-lookup"><span data-stu-id="28b07-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="28b07-108">Definisce un evento specifico dell'attività che il provider è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="28b07-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="28b07-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="28b07-109">Child elements</span></span>



| <span data-ttu-id="28b07-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="28b07-110">Element</span></span>                                                                      | <span data-ttu-id="28b07-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="28b07-111">Type</span></span>                                                                               | <span data-ttu-id="28b07-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28b07-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="28b07-113">**event**</span><span class="sxs-lookup"><span data-stu-id="28b07-113">**event**</span></span>                                                                    | [<span data-ttu-id="28b07-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="28b07-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="28b07-115">Evento specifico dell'attività pubblicato con un'attività.</span><span class="sxs-lookup"><span data-stu-id="28b07-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="28b07-116">**codice operativo**</span><span class="sxs-lookup"><span data-stu-id="28b07-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="28b07-117">Codice operativo specifico dell'attività per un evento.</span><span class="sxs-lookup"><span data-stu-id="28b07-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="28b07-118">Attributi</span><span class="sxs-lookup"><span data-stu-id="28b07-118">Attributes</span></span>



| <span data-ttu-id="28b07-119">Nome</span><span class="sxs-lookup"><span data-stu-id="28b07-119">Name</span></span> | <span data-ttu-id="28b07-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="28b07-120">Type</span></span>      | <span data-ttu-id="28b07-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28b07-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="28b07-122">name</span><span class="sxs-lookup"><span data-stu-id="28b07-122">name</span></span> | <span data-ttu-id="28b07-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="28b07-123">**QName**</span></span> | <span data-ttu-id="28b07-124">Nome del codice operativo specifico dell'attività.</span><span class="sxs-lookup"><span data-stu-id="28b07-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="28b07-125">name</span><span class="sxs-lookup"><span data-stu-id="28b07-125">name</span></span> | <span data-ttu-id="28b07-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="28b07-126">anyURI</span></span>    | <span data-ttu-id="28b07-127">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="28b07-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="28b07-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28b07-128">Requirements</span></span>



| <span data-ttu-id="28b07-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b07-129">Requirement</span></span> | <span data-ttu-id="28b07-130">Valore</span><span class="sxs-lookup"><span data-stu-id="28b07-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="28b07-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28b07-131">Minimum supported client</span></span><br/> | <span data-ttu-id="28b07-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28b07-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="28b07-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28b07-133">Minimum supported server</span></span><br/> | <span data-ttu-id="28b07-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28b07-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





