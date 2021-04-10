---
title: Elemento TimeCreated (SystemPropertiesType)
description: Timestamp che identifica il momento in cui l'evento è stato registrato.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog elemento TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964406"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="23cb6-104">Elemento TimeCreated (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="23cb6-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="23cb6-105">Timestamp che identifica il momento in cui l'evento è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="23cb6-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="23cb6-106">L'elemento **TimeCreated** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="23cb6-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="23cb6-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="23cb6-107">Attributes</span></span>



| <span data-ttu-id="23cb6-108">Nome</span><span class="sxs-lookup"><span data-stu-id="23cb6-108">Name</span></span>       | <span data-ttu-id="23cb6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="23cb6-109">Type</span></span>     | <span data-ttu-id="23cb6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23cb6-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="23cb6-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="23cb6-111">SystemTime</span></span> | <span data-ttu-id="23cb6-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="23cb6-112">dateTime</span></span> | <span data-ttu-id="23cb6-113">Ora di sistema del momento in cui l'evento è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="23cb6-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="23cb6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23cb6-114">Requirements</span></span>



| <span data-ttu-id="23cb6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cb6-115">Requirement</span></span> | <span data-ttu-id="23cb6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="23cb6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23cb6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cb6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="23cb6-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23cb6-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23cb6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cb6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="23cb6-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23cb6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23cb6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23cb6-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="23cb6-122">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="23cb6-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="23cb6-123">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="23cb6-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





