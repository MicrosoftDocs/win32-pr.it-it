---
title: Tipo complesso EventDataType
description: Definisce gli elementi e le strutture dei dati dell'evento che contiene i dati dell'evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- Log eventi di tipo complesso EventDataType
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740375"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="f4696-104">Tipo complesso EventDataType</span><span class="sxs-lookup"><span data-stu-id="f4696-104">EventDataType Complex Type</span></span>

<span data-ttu-id="f4696-105">Definisce gli elementi e le strutture dei dati dell'evento che contiene i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="f4696-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f4696-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f4696-106">Child elements</span></span>



| <span data-ttu-id="f4696-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f4696-107">Element</span></span>                                                              | <span data-ttu-id="f4696-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4696-108">Type</span></span>                                                               | <span data-ttu-id="f4696-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4696-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4696-110">**Binary**</span><span class="sxs-lookup"><span data-stu-id="f4696-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="f4696-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="f4696-111">hexBinary</span></span>                                                          | <span data-ttu-id="f4696-112">BLOB di dati binari per gli eventi scritti mediante la [registrazione degli eventi](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="f4696-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="f4696-113">**ComplexData**</span><span class="sxs-lookup"><span data-stu-id="f4696-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="f4696-114">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="f4696-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="f4696-115">Struttura definita nel modello per l'evento.</span><span class="sxs-lookup"><span data-stu-id="f4696-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="f4696-116">**Data**</span><span class="sxs-lookup"><span data-stu-id="f4696-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="f4696-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f4696-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="f4696-118">Elemento di dati di primo livello definito nel modello per l'evento.</span><span class="sxs-lookup"><span data-stu-id="f4696-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="f4696-119">Attributi</span><span class="sxs-lookup"><span data-stu-id="f4696-119">Attributes</span></span>



| <span data-ttu-id="f4696-120">Nome</span><span class="sxs-lookup"><span data-stu-id="f4696-120">Name</span></span> | <span data-ttu-id="f4696-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4696-121">Type</span></span>   | <span data-ttu-id="f4696-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4696-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="f4696-123">Nome</span><span class="sxs-lookup"><span data-stu-id="f4696-123">Name</span></span> | <span data-ttu-id="f4696-124">stringa</span><span class="sxs-lookup"><span data-stu-id="f4696-124">string</span></span> | <span data-ttu-id="f4696-125">Nome del modello che contiene gli elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="f4696-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f4696-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4696-126">Remarks</span></span>

<span data-ttu-id="f4696-127">La funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering di matrici e strutture come BLOB binari.</span><span class="sxs-lookup"><span data-stu-id="f4696-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4696-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4696-128">Requirements</span></span>



| <span data-ttu-id="f4696-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4696-129">Requirement</span></span> | <span data-ttu-id="f4696-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f4696-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4696-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4696-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f4696-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4696-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4696-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4696-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f4696-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4696-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

