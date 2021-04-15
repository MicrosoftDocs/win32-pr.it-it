---
title: Tipo complesso EventType
description: Definisce il nodo radice dello schema dell'evento.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- Log eventi di tipo complesso EventType
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400298"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="229e8-104">Tipo complesso EventType</span><span class="sxs-lookup"><span data-stu-id="229e8-104">EventType Complex Type</span></span>

<span data-ttu-id="229e8-105">Definisce il nodo radice dello schema dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="229e8-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="229e8-106">Child elements</span></span>



| <span data-ttu-id="229e8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="229e8-107">Element</span></span>                                                                          | <span data-ttu-id="229e8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="229e8-108">Type</span></span>                                                                               | <span data-ttu-id="229e8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="229e8-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="229e8-110">**BinaryEventData**</span><span class="sxs-lookup"><span data-stu-id="229e8-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="229e8-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="229e8-111">hexBinary</span></span>                                                                          | <span data-ttu-id="229e8-112">Contiene i dati dell'evento come BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="229e8-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="229e8-113">Il rendering dei dati dell'evento viene eseguito come BLOB binario se la funzione di rendering non riesce a trovare i metadati utilizzati per decodificare l'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="229e8-114">**DebugData**</span><span class="sxs-lookup"><span data-stu-id="229e8-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="229e8-115">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="229e8-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="229e8-116">Contiene i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="229e8-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="229e8-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="229e8-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="229e8-118">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="229e8-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="229e8-119">Contiene i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-119">Contains the event data.</span></span> <span data-ttu-id="229e8-120">L'ordine degli elementi di dati nel modello determina il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="229e8-121">**ProcessingErrorData**</span><span class="sxs-lookup"><span data-stu-id="229e8-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="229e8-122">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="229e8-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="229e8-123">Contiene i dettagli dell'errore che si è verificato durante il tentativo di eseguire il rendering dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="229e8-124">Questa situazione può verificarsi se i dati dell'evento non corrispondono alla definizione dei dati dell'evento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="229e8-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="229e8-125">I dati dell'evento sono inclusi come BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="229e8-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="229e8-126">**RenderingInfo**</span><span class="sxs-lookup"><span data-stu-id="229e8-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="229e8-127">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="229e8-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="229e8-128">Contiene le stringhe di messaggio di cui è stato eseguito il rendering per l'evento (include la stringa di messaggio dell'evento e le stringhe di messaggio per qualsiasi proprietà dell'evento, ad esempio Level, Task e OpCode).</span><span class="sxs-lookup"><span data-stu-id="229e8-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="229e8-129">Questa sezione contiene solo gli eventi che sono stati raccolti tramite il servizio [raccolta eventi di Windows](/windows/desktop/WEC/windows-event-collector) .</span><span class="sxs-lookup"><span data-stu-id="229e8-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="229e8-130">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="229e8-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="229e8-131">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="229e8-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="229e8-132">Contiene informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.</span><span class="sxs-lookup"><span data-stu-id="229e8-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="229e8-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="229e8-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="229e8-134">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="229e8-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="229e8-135">Contiene i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-135">Contains the event data.</span></span> <span data-ttu-id="229e8-136">La sezione dei dati utente del modello determina il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="229e8-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="229e8-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="229e8-137">Remarks</span></span>

<span data-ttu-id="229e8-138">In genere, questa sezione conterrà con la sezione **EventData** o **UserData** .</span><span class="sxs-lookup"><span data-stu-id="229e8-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="229e8-139">La sezione **EventData** viene utilizzata se il modello non contiene una sezione **UserData** .</span><span class="sxs-lookup"><span data-stu-id="229e8-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="229e8-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="229e8-140">Requirements</span></span>



| <span data-ttu-id="229e8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="229e8-141">Requirement</span></span> | <span data-ttu-id="229e8-142">Valore</span><span class="sxs-lookup"><span data-stu-id="229e8-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="229e8-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229e8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="229e8-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="229e8-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="229e8-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="229e8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="229e8-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="229e8-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

