---
title: Elemento RenderingInfo (EventType)
description: Contiene le stringhe di messaggio di cui è stato eseguito il rendering per l'evento (include la stringa di messaggio dell'evento e le stringhe di messaggio per qualsiasi proprietà dell'evento, ad esempio Level, Task e OpCode).
ms.assetid: a0b2a21d-16a0-4c88-9d57-4c99706eeea1
keywords:
- EventLog elemento RenderingInfo
topic_type:
- apiref
api_name:
- RenderingInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 771901196c4988025cce203ffc3134450d38ed7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340293"
---
# <a name="renderinginfo-eventtype-element"></a><span data-ttu-id="2c768-104">Elemento RenderingInfo (EventType)</span><span class="sxs-lookup"><span data-stu-id="2c768-104">RenderingInfo (EventType) Element</span></span>

<span data-ttu-id="2c768-105">Contiene le stringhe di messaggio di cui è stato eseguito il rendering per l'evento (include la stringa di messaggio dell'evento e le stringhe di messaggio per qualsiasi proprietà dell'evento, ad esempio Level, Task e OpCode).</span><span class="sxs-lookup"><span data-stu-id="2c768-105">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span>

``` syntax
<xs:element name="RenderingInfo"
    type="RenderingType"
 />
```

<span data-ttu-id="2c768-106">L'elemento **RenderingInfo** è definito dal tipo complesso [**eventType**](eventschema-eventtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c768-106">The **RenderingInfo** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c768-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c768-107">Requirements</span></span>



| <span data-ttu-id="2c768-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c768-108">Requirement</span></span> | <span data-ttu-id="2c768-109">Valore</span><span class="sxs-lookup"><span data-stu-id="2c768-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c768-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c768-110">Minimum supported client</span></span><br/> | <span data-ttu-id="2c768-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c768-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c768-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c768-112">Minimum supported server</span></span><br/> | <span data-ttu-id="2c768-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c768-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c768-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c768-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c768-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="2c768-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2c768-116">**event**</span><span class="sxs-lookup"><span data-stu-id="2c768-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





