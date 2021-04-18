---
title: Tipo complesso ChannelPublishingType
description: Definisce le proprietà di registrazione per la sessione utilizzata dal canale. | Tipo complesso ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Log eventi di tipo complesso ChannelPublishingType
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321735"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="97f6e-105">Tipo complesso ChannelPublishingType</span><span class="sxs-lookup"><span data-stu-id="97f6e-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="97f6e-106">Definisce le proprietà di registrazione per la sessione utilizzata dal canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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

## <a name="child-elements"></a><span data-ttu-id="97f6e-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="97f6e-107">Child elements</span></span>



| <span data-ttu-id="97f6e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="97f6e-108">Element</span></span>                                                                              | <span data-ttu-id="97f6e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="97f6e-109">Type</span></span>                                                              | <span data-ttu-id="97f6e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97f6e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97f6e-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="97f6e-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="97f6e-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="97f6e-113">Quantità di memoria, in kilobyte, da allocare per ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="97f6e-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="97f6e-114">Se si prevede una frequenza di eventi relativamente bassa, le dimensioni del buffer devono essere impostate sulle dimensioni della pagina di memoria.</span><span class="sxs-lookup"><span data-stu-id="97f6e-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="97f6e-115">Se la frequenza degli eventi dovrebbe essere relativamente elevata, è necessario specificare una dimensione del buffer maggiore e aumentare il numero massimo di buffer.</span><span class="sxs-lookup"><span data-stu-id="97f6e-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="97f6e-116">La dimensione del buffer influiscono sulla velocità di riempimento dei buffer e deve essere scaricata.</span><span class="sxs-lookup"><span data-stu-id="97f6e-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="97f6e-117">Sebbene le dimensioni di un buffer di piccole dimensioni richiedano meno memoria, aumentano la velocità con cui è necessario scaricare i buffer.</span><span class="sxs-lookup"><span data-stu-id="97f6e-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="97f6e-118">Le dimensioni predefinite del buffer per i canali analitici e di debug sono pari a 4 KB e per l'amministratore e la relativa operatività è 64 KB.</span><span class="sxs-lookup"><span data-stu-id="97f6e-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="97f6e-119">**clockType**</span><span class="sxs-lookup"><span data-stu-id="97f6e-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="97f6e-120">Risoluzione del clock da usare quando si registra il timestamp per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="97f6e-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="97f6e-121">È possibile specificare SystemTime o QPC.</span><span class="sxs-lookup"><span data-stu-id="97f6e-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="97f6e-122">SystemTime fornisce un indicatore di tempo a bassa risoluzione (10 millisecondi), ma è relativamente meno costoso da recuperare.</span><span class="sxs-lookup"><span data-stu-id="97f6e-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="97f6e-123">Il valore predefinito è SystemTime.</span><span class="sxs-lookup"><span data-stu-id="97f6e-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="97f6e-124">Il contatore delle prestazioni delle query (QPC) fornisce un timestamp ad alta risoluzione (100 nanosecondi), ma è relativamente più costoso da recuperare.</span><span class="sxs-lookup"><span data-stu-id="97f6e-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="97f6e-125">È necessario QPC se si dispone di un elevato tasso di eventi o se il consumer unisce gli eventi da buffer diversi.</span><span class="sxs-lookup"><span data-stu-id="97f6e-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="97f6e-126">**controlGuid**</span><span class="sxs-lookup"><span data-stu-id="97f6e-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="97f6e-127">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="97f6e-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="97f6e-128">Identifica il GUID della sessione per una sessione ETW che contiene eventi WPP.</span><span class="sxs-lookup"><span data-stu-id="97f6e-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="97f6e-129">Questa impostazione è consentita solo per i canali di tipo debug.</span><span class="sxs-lookup"><span data-stu-id="97f6e-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="97f6e-130">Non è possibile abilitare completamente questi canali con le parole chiave impostate su zero (0x0000000000000000).</span><span class="sxs-lookup"><span data-stu-id="97f6e-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="97f6e-131">Devono essere abilitate con le parole chiave impostate su 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="97f6e-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="97f6e-132">**fileMax**</span><span class="sxs-lookup"><span data-stu-id="97f6e-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="97f6e-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="97f6e-134">Il numero massimo di volte in cui si desidera che il servizio crei un nuovo file di log quando il canale è abilitato (incluso quando il computer viene riavviato).</span><span class="sxs-lookup"><span data-stu-id="97f6e-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="97f6e-135">Se il valore è 0 o 1, il servizio sovrascriverà il file di log ogni volta che il canale viene abilitato e gli eventi precedenti andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="97f6e-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="97f6e-136">Se il valore è maggiore di 1, il servizio creerà un nuovo file di log ogni volta che il canale viene abilitato per mantenere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="97f6e-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="97f6e-137">Il valore predefinito è 1 e il valore massimo che è possibile specificare è 16.</span><span class="sxs-lookup"><span data-stu-id="97f6e-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="97f6e-138">Il servizio aggiunge un numero decimale a tre cifre compreso tra 0 e fileMax 1 e il nome di ogni file.</span><span class="sxs-lookup"><span data-stu-id="97f6e-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="97f6e-139">Ad esempio *filename*. etl.xxx, dove xxx è il numero decimale a tre cifre.</span><span class="sxs-lookup"><span data-stu-id="97f6e-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="97f6e-140">I file si trovano in% windir% \\ system32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="97f6e-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="97f6e-141">**Parole**</span><span class="sxs-lookup"><span data-stu-id="97f6e-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="97f6e-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="97f6e-143">Maschera di maschera che determina la categoria di eventi scritti nel canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="97f6e-144">Se il valore dell'attributo **Keywords** è 0, tutti gli eventi scritti dal provider vengono scritti nel canale. in caso contrario, solo gli eventi che hanno definito una parola chiave inclusa nella maschera di **parole chiave** vengono scritti nel canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="97f6e-145">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="97f6e-145">The default is 0.</span></span><br/> <span data-ttu-id="97f6e-146">I canali di debug per i quali è impostato l'attributo controlGuid devono impostare l'attributo **Keywords** su 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="97f6e-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="97f6e-147">La sessione passa il valore Keywords al provider quando Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="97f6e-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="97f6e-148">**latenza**</span><span class="sxs-lookup"><span data-stu-id="97f6e-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="97f6e-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="97f6e-150">Tempo di attesa prima dello scaricamento dei buffer, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="97f6e-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="97f6e-151">Se è zero, ETW Scarica i buffer non appena diventano pieni.</span><span class="sxs-lookup"><span data-stu-id="97f6e-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="97f6e-152">Se è diverso da zero, ETW Scarica tutti i buffer che contengono eventi in base al valore anche se il buffer non è pieno.</span><span class="sxs-lookup"><span data-stu-id="97f6e-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="97f6e-153">In genere, si desidera scaricare i buffer solo quando diventano pieni.</span><span class="sxs-lookup"><span data-stu-id="97f6e-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="97f6e-154">La forzatura dei buffer per lo scaricamento può aumentare le dimensioni del file di log con lo spazio del buffer non riempito.</span><span class="sxs-lookup"><span data-stu-id="97f6e-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="97f6e-155">Il valore predefinito è 1 secondo per i log amministrativi e operativi e 5 secondi per i log analitici e di debug.</span><span class="sxs-lookup"><span data-stu-id="97f6e-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="97f6e-156">**livello**</span><span class="sxs-lookup"><span data-stu-id="97f6e-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="97f6e-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="97f6e-158">Livello di gravità degli eventi da scrivere sul canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="97f6e-159">Il servizio scrive gli eventi nel canale che hanno un valore di livello minore o uguale al valore specificato.</span><span class="sxs-lookup"><span data-stu-id="97f6e-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="97f6e-160">Il valore predefinito è 0, che indica la registrazione di eventi con qualsiasi valore di livello.</span><span class="sxs-lookup"><span data-stu-id="97f6e-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="97f6e-161">La sessione passa il valore del livello al provider quando Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="97f6e-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="97f6e-162">**maxBuffers**</span><span class="sxs-lookup"><span data-stu-id="97f6e-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="97f6e-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="97f6e-164">Numero massimo di buffer da allocare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="97f6e-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="97f6e-165">In genere, questo valore è il numero minimo di buffer più venti.</span><span class="sxs-lookup"><span data-stu-id="97f6e-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="97f6e-166">Questo valore deve essere maggiore o uguale al valore specificato per minBuffers.</span><span class="sxs-lookup"><span data-stu-id="97f6e-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="97f6e-167">Il numero massimo predefinito di buffer per i canali analitici e di debug è 10 KB e per l'amministratore e operativo è 64 KB.</span><span class="sxs-lookup"><span data-stu-id="97f6e-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="97f6e-168">**minBuffers**</span><span class="sxs-lookup"><span data-stu-id="97f6e-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="97f6e-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="97f6e-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="97f6e-170">Numero minimo di buffer da allocare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="97f6e-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="97f6e-171">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="97f6e-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="97f6e-172">**sidType**</span><span class="sxs-lookup"><span data-stu-id="97f6e-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="97f6e-173">Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="97f6e-174">Per includere il SID con l'evento, impostare questo attributo su "Publishing".</span><span class="sxs-lookup"><span data-stu-id="97f6e-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="97f6e-175">Il SID viene impostato in base all'identità del thread nel momento in cui viene scritto l'evento.</span><span class="sxs-lookup"><span data-stu-id="97f6e-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="97f6e-176">Se non si desidera includere il SID con l'evento, impostare questo attributo su "None".</span><span class="sxs-lookup"><span data-stu-id="97f6e-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="97f6e-177">Il valore predefinito è "Publishing".</span><span class="sxs-lookup"><span data-stu-id="97f6e-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="97f6e-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="97f6e-178">Remarks</span></span>

<span data-ttu-id="97f6e-179">È possibile specificare queste informazioni di pubblicazione per i tipi di canale analitico e di debug o per qualsiasi canale che specifichi l'isolamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="97f6e-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="97f6e-180">Sebbene sia possibile specificare il livello e le parole chiave, è necessario considerare che questi saranno gli unici eventi che si riceveranno dal provider per il canale.</span><span class="sxs-lookup"><span data-stu-id="97f6e-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="97f6e-181">Quando un buffer è pieno, ETW Scarica il buffer nel file di log.</span><span class="sxs-lookup"><span data-stu-id="97f6e-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="97f6e-182">Se i buffer vengono compilati più velocemente di quanto possano essere scaricati, i nuovi buffer vengono allocati e aggiunti al pool di buffer della sessione, fino al numero massimo specificato.</span><span class="sxs-lookup"><span data-stu-id="97f6e-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="97f6e-183">Oltre questo limite, la sessione ignora gli eventi in ingresso fino a quando non diventa disponibile un buffer.</span><span class="sxs-lookup"><span data-stu-id="97f6e-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f6e-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97f6e-184">Requirements</span></span>



| <span data-ttu-id="97f6e-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="97f6e-185">Requirement</span></span> | <span data-ttu-id="97f6e-186">Valore</span><span class="sxs-lookup"><span data-stu-id="97f6e-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97f6e-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97f6e-187">Minimum supported client</span></span><br/> | <span data-ttu-id="97f6e-188">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97f6e-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97f6e-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97f6e-189">Minimum supported server</span></span><br/> | <span data-ttu-id="97f6e-190">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97f6e-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





