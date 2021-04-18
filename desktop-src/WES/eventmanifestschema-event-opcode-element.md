---
title: evento (OpCode) (elemento)
description: Definisce un evento per un codice operativo specifico di un'attività.
ms.assetid: 7ca8fff2-ef1a-45c4-b082-e4745330bf0b
keywords:
- EventLog elemento evento
topic_type:
- apiref
api_name:
- event
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25f7a7f3a92c07895529d6dad59df22a7389735d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302665"
---
# <a name="event-opcode-element"></a><span data-ttu-id="53d18-104">evento (OpCode) (elemento)</span><span class="sxs-lookup"><span data-stu-id="53d18-104">event (opcode) Element</span></span>

<span data-ttu-id="53d18-105">\[A partire dal compilatore di messaggi fornito con la versione di Windows 7 del Windows SDK, questo elemento non è più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="53d18-105">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="53d18-106">Definisce un evento per un codice operativo specifico di un'attività.</span><span class="sxs-lookup"><span data-stu-id="53d18-106">Defines an event for a task-specific opcode.</span></span>

``` syntax
<xs:element name="event"
    type="EventDefinitionType"
 />
```

<span data-ttu-id="53d18-107">L'elemento **Event** viene definito dall'elemento [**OpCode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="53d18-107">The **event** element is defined by the [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d18-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53d18-108">Requirements</span></span>



| <span data-ttu-id="53d18-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="53d18-109">Requirement</span></span> | <span data-ttu-id="53d18-110">Valore</span><span class="sxs-lookup"><span data-stu-id="53d18-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53d18-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d18-111">Minimum supported client</span></span><br/> | <span data-ttu-id="53d18-112">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53d18-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53d18-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53d18-113">Minimum supported server</span></span><br/> | <span data-ttu-id="53d18-114">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53d18-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53d18-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53d18-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="53d18-116">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="53d18-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="53d18-117">**opcode (TaskEventDefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="53d18-117">**opcode (TaskEventDefinitionType)**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





