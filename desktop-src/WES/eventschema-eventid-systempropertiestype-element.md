---
title: Elemento EventId (SystemPropertiesType)
description: Identificatore utilizzato dal provider per identificare l'evento.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- Evento EventId elemento EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475598"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="2bc55-104">Elemento EventId (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="2bc55-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="2bc55-105">Identificatore utilizzato dal provider per identificare l'evento.</span><span class="sxs-lookup"><span data-stu-id="2bc55-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2bc55-106">L'elemento **eventId** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2bc55-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc55-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bc55-107">Requirements</span></span>



| <span data-ttu-id="2bc55-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc55-108">Requirement</span></span> | <span data-ttu-id="2bc55-109">Valore</span><span class="sxs-lookup"><span data-stu-id="2bc55-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bc55-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bc55-110">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc55-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bc55-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2bc55-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bc55-112">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc55-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2bc55-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bc55-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bc55-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bc55-115">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="2bc55-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2bc55-116">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="2bc55-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





