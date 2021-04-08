---
title: Elemento provider (SystemPropertiesType)
description: Identifica il provider che ha registrato l'evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- EventLog elemento provider
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048017"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="59766-104">Elemento provider (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="59766-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="59766-105">Identifica il provider che ha registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="59766-105">Identifies the provider that logged the event.</span></span>

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="59766-106">L'elemento **provider** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="59766-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="59766-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="59766-107">Attributes</span></span>



| <span data-ttu-id="59766-108">Nome</span><span class="sxs-lookup"><span data-stu-id="59766-108">Name</span></span>            | <span data-ttu-id="59766-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="59766-109">Type</span></span>                                                | <span data-ttu-id="59766-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59766-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59766-111">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="59766-111">EventSourceName</span></span> | <span data-ttu-id="59766-112">string</span><span class="sxs-lookup"><span data-stu-id="59766-112">string</span></span>                                              | <span data-ttu-id="59766-113">Nome dell'origine evento che ha pubblicato l'evento (se l'origine evento è dall'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) legacy).</span><span class="sxs-lookup"><span data-stu-id="59766-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="59766-114">Guid</span><span class="sxs-lookup"><span data-stu-id="59766-114">Guid</span></span>            | [<span data-ttu-id="59766-115">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="59766-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="59766-116">Identificatore univoco globale che identifica in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="59766-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="59766-117">Nome</span><span class="sxs-lookup"><span data-stu-id="59766-117">Name</span></span>            | <span data-ttu-id="59766-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="59766-118">anyURI</span></span>                                              | <span data-ttu-id="59766-119">Nome del provider di eventi che ha registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="59766-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="59766-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59766-120">Requirements</span></span>



| <span data-ttu-id="59766-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="59766-121">Requirement</span></span> | <span data-ttu-id="59766-122">Valore</span><span class="sxs-lookup"><span data-stu-id="59766-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59766-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59766-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59766-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59766-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59766-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59766-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59766-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59766-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59766-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59766-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="59766-128">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="59766-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="59766-129">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="59766-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

