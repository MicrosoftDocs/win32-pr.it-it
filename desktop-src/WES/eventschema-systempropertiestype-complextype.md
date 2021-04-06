---
title: Tipo complesso SystemPropertiesType
description: Definisce le informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Log eventi di tipo complesso SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742722"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="0fc68-104">Tipo complesso SystemPropertiesType</span><span class="sxs-lookup"><span data-stu-id="0fc68-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="0fc68-105">Definisce le informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.</span><span class="sxs-lookup"><span data-stu-id="0fc68-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
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
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0fc68-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0fc68-106">Child elements</span></span>



| <span data-ttu-id="0fc68-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0fc68-107">Element</span></span>                                                                         | <span data-ttu-id="0fc68-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fc68-108">Type</span></span>                                                        | <span data-ttu-id="0fc68-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fc68-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fc68-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="0fc68-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="0fc68-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="0fc68-111">anyURI</span></span>                                                      | <span data-ttu-id="0fc68-112">Canale in cui è stato registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="0fc68-113">**Computer**</span><span class="sxs-lookup"><span data-stu-id="0fc68-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="0fc68-114">string</span><span class="sxs-lookup"><span data-stu-id="0fc68-114">string</span></span>                                                      | <span data-ttu-id="0fc68-115">nome del computer in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="0fc68-116">**Correlazione**</span><span class="sxs-lookup"><span data-stu-id="0fc68-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="0fc68-117">Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.</span><span class="sxs-lookup"><span data-stu-id="0fc68-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="0fc68-118">**EventID**</span><span class="sxs-lookup"><span data-stu-id="0fc68-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="0fc68-119">Identificatore utilizzato dal provider per identificare l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0fc68-120">**EventRecordID**</span><span class="sxs-lookup"><span data-stu-id="0fc68-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="0fc68-121">Numero di record assegnato all'evento quando è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="0fc68-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="0fc68-122">**Esecuzione**</span><span class="sxs-lookup"><span data-stu-id="0fc68-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="0fc68-123">Contiene informazioni sul processo e sul thread che hanno registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="0fc68-124">**Parole chiave**</span><span class="sxs-lookup"><span data-stu-id="0fc68-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="0fc68-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="0fc68-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="0fc68-126">Maschera di maschera delle parole chiave definite nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="0fc68-127">Le parole chiave vengono utilizzate per classificare i tipi di eventi (ad esempio, gli eventi associati alla lettura dei dati).</span><span class="sxs-lookup"><span data-stu-id="0fc68-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="0fc68-128">**Livello**</span><span class="sxs-lookup"><span data-stu-id="0fc68-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="0fc68-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0fc68-129">unsignedByte</span></span>                                                | <span data-ttu-id="0fc68-130">Livello di gravità definito nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="0fc68-131">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="0fc68-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="0fc68-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0fc68-132">unsignedByte</span></span>                                                | <span data-ttu-id="0fc68-133">Codice operativo definito nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-133">The opcode defined in the event.</span></span> <span data-ttu-id="0fc68-134">Task e OpCode sono typcially usati per identificare la posizione nell'applicazione dalla quale è stato registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="0fc68-135">**Provider**</span><span class="sxs-lookup"><span data-stu-id="0fc68-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="0fc68-136">Identifica il provider che ha registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="0fc68-137">Gli attributi **Name** e **GUID** sono inclusi se il provider utilizza un manifesto di strumentazione per definire gli eventi; in caso contrario, l'attributo **eventSourceName** viene incluso se un provider di eventi legacy (usando l'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) ) ha registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="0fc68-138">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="0fc68-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="0fc68-139">Identifica l'utente che ha registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="0fc68-140">**Attività**</span><span class="sxs-lookup"><span data-stu-id="0fc68-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="0fc68-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0fc68-141">unsignedShort</span></span>                                               | <span data-ttu-id="0fc68-142">Attività definita nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-142">The task defined in the event.</span></span> <span data-ttu-id="0fc68-143">L'attività e il codice operativo vengono in genere utilizzati per identificare la posizione nell'applicazione dalla quale è stato registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="0fc68-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="0fc68-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="0fc68-145">Timestamp che identifica il momento in cui l'evento è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="0fc68-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="0fc68-146">Il timestamp includerà l'attributo **SYSTEMTIME** o l'attributo **RawTime** .</span><span class="sxs-lookup"><span data-stu-id="0fc68-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="0fc68-147">**Versione**</span><span class="sxs-lookup"><span data-stu-id="0fc68-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="0fc68-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0fc68-148">unsignedByte</span></span>                                                | <span data-ttu-id="0fc68-149">Numero di versione della definizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="0fc68-150">Attributi</span><span class="sxs-lookup"><span data-stu-id="0fc68-150">Attributes</span></span>



| <span data-ttu-id="0fc68-151">Nome</span><span class="sxs-lookup"><span data-stu-id="0fc68-151">Name</span></span>              | <span data-ttu-id="0fc68-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fc68-152">Type</span></span>                                                | <span data-ttu-id="0fc68-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fc68-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc68-154">ActivityID</span><span class="sxs-lookup"><span data-stu-id="0fc68-154">ActivityID</span></span>        | [<span data-ttu-id="0fc68-155">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="0fc68-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="0fc68-156">Identificatore univoco globale che identifica l'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="0fc68-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="0fc68-157">Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.</span><span class="sxs-lookup"><span data-stu-id="0fc68-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="0fc68-158">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="0fc68-158">EventSourceName</span></span>   | <span data-ttu-id="0fc68-159">string</span><span class="sxs-lookup"><span data-stu-id="0fc68-159">string</span></span>                                              | <span data-ttu-id="0fc68-160">Nome dell'origine evento che ha pubblicato l'evento (se l'origine evento è dall'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) legacy).</span><span class="sxs-lookup"><span data-stu-id="0fc68-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="0fc68-161">Guid</span><span class="sxs-lookup"><span data-stu-id="0fc68-161">Guid</span></span>              | [<span data-ttu-id="0fc68-162">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="0fc68-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="0fc68-163">Identificatore univoco globale che identifica in modo univoco il provider.</span><span class="sxs-lookup"><span data-stu-id="0fc68-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="0fc68-164">KernelTime</span><span class="sxs-lookup"><span data-stu-id="0fc68-164">KernelTime</span></span>        | <span data-ttu-id="0fc68-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-165">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-166">Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in unità di tempo della CPU.</span><span class="sxs-lookup"><span data-stu-id="0fc68-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="0fc68-167">Se si utilizza una sessione privata ETW, utilizzare invece il valore del membro ProcessorTime.</span><span class="sxs-lookup"><span data-stu-id="0fc68-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="0fc68-168">Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).</span><span class="sxs-lookup"><span data-stu-id="0fc68-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="0fc68-169">Nome</span><span class="sxs-lookup"><span data-stu-id="0fc68-169">Name</span></span>              | <span data-ttu-id="0fc68-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="0fc68-170">anyURI</span></span>                                              | <span data-ttu-id="0fc68-171">Nome del provider.</span><span class="sxs-lookup"><span data-stu-id="0fc68-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0fc68-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="0fc68-172">ProcessID</span></span>         | <span data-ttu-id="0fc68-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-173">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-174">Identifica il processo che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="0fc68-175">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="0fc68-175">ProcessorID</span></span>       | <span data-ttu-id="0fc68-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="0fc68-176">unsignedByte</span></span>                                        | <span data-ttu-id="0fc68-177">Numero di identificazione del processore che ha elaborato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="0fc68-178">Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).</span><span class="sxs-lookup"><span data-stu-id="0fc68-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="0fc68-179">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="0fc68-179">ProcessorTime</span></span>     | <span data-ttu-id="0fc68-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-180">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-181">Per le sessioni private ETW, il tempo di esecuzione trascorso per le istruzioni in modalità utente, in cicli della CPU.</span><span class="sxs-lookup"><span data-stu-id="0fc68-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="0fc68-182">Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).</span><span class="sxs-lookup"><span data-stu-id="0fc68-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="0fc68-183">Qualificatori</span><span class="sxs-lookup"><span data-stu-id="0fc68-183">Qualifiers</span></span>        | <span data-ttu-id="0fc68-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="0fc68-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="0fc68-185">Un provider Legacy utilizza un numero a 32 bit per identificare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0fc68-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="0fc68-186">Se l'evento viene registrato da un provider Legacy, il valore dell'elemento **eventId** contiene i 16 bit di ordine inferiore dell'identificatore dell'evento e l'attributo **Qualifier** contiene i 16 bit più significativi dell'identificatore di evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="0fc68-187">RawTime</span><span class="sxs-lookup"><span data-stu-id="0fc68-187">RawTime</span></span>           | <span data-ttu-id="0fc68-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="0fc68-188">unsignedLong</span></span>                                        | <span data-ttu-id="0fc68-189">Valore del timestamp non elaborato; il formato del timestamp dipende dall'origine dell'ora utilizzata per raccogliere la traccia.</span><span class="sxs-lookup"><span data-stu-id="0fc68-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="0fc68-190">Il timestamp non elaborato offre una precisione maggiore rispetto all'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fc68-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="0fc68-191">L'output dell'evento di cui è stato eseguito il rendering conterrà solo l'ora RAW se si usa TraceRpt.exe con l'opzione-RTS.</span><span class="sxs-lookup"><span data-stu-id="0fc68-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="0fc68-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="0fc68-192">RelatedActivityID</span></span> | [<span data-ttu-id="0fc68-193">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="0fc68-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="0fc68-194">Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo.</span><span class="sxs-lookup"><span data-stu-id="0fc68-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="0fc68-195">Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.</span><span class="sxs-lookup"><span data-stu-id="0fc68-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="0fc68-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="0fc68-196">SessionID</span></span>         | <span data-ttu-id="0fc68-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-197">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-198">Numero di identificazione per la sessione di Terminal Server in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="0fc68-199">Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).</span><span class="sxs-lookup"><span data-stu-id="0fc68-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="0fc68-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="0fc68-200">SystemTime</span></span>        | <span data-ttu-id="0fc68-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="0fc68-201">dateTime</span></span>                                            | <span data-ttu-id="0fc68-202">Ora di sistema del momento in cui l'evento è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="0fc68-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="0fc68-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="0fc68-203">ThreadID</span></span>          | <span data-ttu-id="0fc68-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-204">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-205">Identifica il thread che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="0fc68-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="0fc68-206">UserID</span><span class="sxs-lookup"><span data-stu-id="0fc68-206">UserID</span></span>            | <span data-ttu-id="0fc68-207">string</span><span class="sxs-lookup"><span data-stu-id="0fc68-207">string</span></span>                                              | <span data-ttu-id="0fc68-208">ID di sicurezza (SID) dell'utente in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="0fc68-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="0fc68-209">Tempi</span><span class="sxs-lookup"><span data-stu-id="0fc68-209">UserTime</span></span>          | <span data-ttu-id="0fc68-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0fc68-210">unsignedInt</span></span>                                         | <span data-ttu-id="0fc68-211">Tempo di esecuzione trascorso per le istruzioni in modalità utente, in unità di tempo della CPU.</span><span class="sxs-lookup"><span data-stu-id="0fc68-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="0fc68-212">Se si utilizza una sessione privata ETW, utilizzare invece il valore del membro ProcessorTime.</span><span class="sxs-lookup"><span data-stu-id="0fc68-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="0fc68-213">Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).</span><span class="sxs-lookup"><span data-stu-id="0fc68-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="0fc68-214">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fc68-214">Remarks</span></span>

<span data-ttu-id="0fc68-215">Per impostazione predefinita, l'evento contiene il nome di dominio completo (FQDN) di un computer.</span><span class="sxs-lookup"><span data-stu-id="0fc68-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="0fc68-216">Per usare il nome NETBIOS anziché il nome di dominio completo, è necessario creare un valore DWORD del registro di sistema denominato CompatFlags nella seguente chiave del registro di sistema e impostare il valore di CompatFlags su 0x2.</span><span class="sxs-lookup"><span data-stu-id="0fc68-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="0fc68-217">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fc68-217">Requirements</span></span>



| <span data-ttu-id="0fc68-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc68-218">Requirement</span></span> | <span data-ttu-id="0fc68-219">Valore</span><span class="sxs-lookup"><span data-stu-id="0fc68-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fc68-220">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fc68-220">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc68-221">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fc68-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0fc68-222">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fc68-222">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc68-223">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fc68-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

