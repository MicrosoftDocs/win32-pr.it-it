---
title: Tipo complesso DefinitionType
description: Definisce un elenco di eventi che il provider può registrare.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- Log eventi di tipo complesso DefinitionType
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301556"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="de937-104">Tipo complesso DefinitionType</span><span class="sxs-lookup"><span data-stu-id="de937-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="de937-105">Definisce un elenco di eventi che il provider può registrare.</span><span class="sxs-lookup"><span data-stu-id="de937-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="de937-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="de937-106">Child elements</span></span>



| <span data-ttu-id="de937-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="de937-107">Element</span></span>                                                           | <span data-ttu-id="de937-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="de937-108">Type</span></span>                                                                                       | <span data-ttu-id="de937-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de937-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de937-110">**evento**</span><span class="sxs-lookup"><span data-stu-id="de937-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="de937-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="de937-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="de937-112">Definisce un evento che il provider è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="de937-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="de937-113">**attività**</span><span class="sxs-lookup"><span data-stu-id="de937-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="de937-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="de937-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="de937-115">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="de937-115">Not supported.</span></span><br/> <span data-ttu-id="de937-116">**Windows Server 2008 e Windows Vista:** Definisce un evento specifico dell'attività che il provider è in grado di registrare.</span><span class="sxs-lookup"><span data-stu-id="de937-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="de937-117">(A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, gli eventi specifici dell'attività non sono più supportati).</span><span class="sxs-lookup"><span data-stu-id="de937-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de937-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de937-118">Requirements</span></span>



| <span data-ttu-id="de937-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de937-119">Requirement</span></span> | <span data-ttu-id="de937-120">Valore</span><span class="sxs-lookup"><span data-stu-id="de937-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de937-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de937-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de937-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de937-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de937-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de937-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de937-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de937-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





