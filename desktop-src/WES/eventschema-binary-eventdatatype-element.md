---
title: Binary (EventDataType)-elemento
description: BLOB di dati binari per gli eventi scritti mediante la registrazione degli eventi.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- EventLog elemento binario
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047874"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="fa7ad-104">Binary (EventDataType)-elemento</span><span class="sxs-lookup"><span data-stu-id="fa7ad-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="fa7ad-105">BLOB di dati binari per gli eventi scritti mediante la [registrazione degli eventi](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="fa7ad-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="fa7ad-106">L'elemento **binario** è definito dal tipo complesso [**EventDataType**](eventschema-eventdatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fa7ad-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7ad-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa7ad-107">Requirements</span></span>



| <span data-ttu-id="fa7ad-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa7ad-108">Requirement</span></span> | <span data-ttu-id="fa7ad-109">Valore</span><span class="sxs-lookup"><span data-stu-id="fa7ad-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa7ad-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa7ad-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fa7ad-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa7ad-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa7ad-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa7ad-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fa7ad-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa7ad-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa7ad-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa7ad-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa7ad-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="fa7ad-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="fa7ad-116">**EventData (EventType)**</span><span class="sxs-lookup"><span data-stu-id="fa7ad-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

