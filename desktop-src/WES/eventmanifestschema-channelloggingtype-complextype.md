---
title: Tipo complesso ChannelLoggingType
description: Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se è sequenziale o circolare. | Tipo complesso ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Log eventi di tipo complesso ChannelLoggingType
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132270"
---
# <a name="channelloggingtype-complex-type"></a><span data-ttu-id="76ff6-105">Tipo complesso ChannelLoggingType</span><span class="sxs-lookup"><span data-stu-id="76ff6-105">ChannelLoggingType Complex Type</span></span>

<span data-ttu-id="76ff6-106">Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se è sequenziale o circolare.</span><span class="sxs-lookup"><span data-stu-id="76ff6-106">Defines the properties of the log file that backs the channel, such as its capacity and whether it is sequential or circular.</span></span>

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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

## <a name="child-elements"></a><span data-ttu-id="76ff6-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="76ff6-107">Child elements</span></span>



| <span data-ttu-id="76ff6-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="76ff6-108">Element</span></span>                                                                         | <span data-ttu-id="76ff6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="76ff6-109">Type</span></span>                                                              | <span data-ttu-id="76ff6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76ff6-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76ff6-111">**Backup automatico**</span><span class="sxs-lookup"><span data-stu-id="76ff6-111">**autoBackup**</span></span>](eventmanifestschema-autobackup-channelloggingtype-element.md) | <span data-ttu-id="76ff6-112">boolean</span><span class="sxs-lookup"><span data-stu-id="76ff6-112">boolean</span></span>                                                           | <span data-ttu-id="76ff6-113">Determina se creare un nuovo file di log quando il file di log corrente raggiunge le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="76ff6-113">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span> <span data-ttu-id="76ff6-114">Impostare su **true** per richiedere che il servizio crei un nuovo file quando il file di log raggiunge la dimensione massima; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="76ff6-114">Set to **true** to request that the service create a new file when the log file reaches its maximum size; otherwise, **false**.</span></span> <span data-ttu-id="76ff6-115">È possibile impostare il [**backup automatico**](eventmanifestschema-autobackup-channelloggingtype-element.md) su **true** solo se la [**conservazione**](eventmanifestschema-retention-channelloggingtype-element.md) è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="76ff6-115">You can set [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) to **true** only if [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) is set to **true**.</span></span> <span data-ttu-id="76ff6-116">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="76ff6-116">The default is **false**.</span></span><br/> <span data-ttu-id="76ff6-117">Non esiste alcun limite al numero di file di backup che il servizio è in grado di creare (limitato solo dallo spazio disponibile su disco).</span><span class="sxs-lookup"><span data-stu-id="76ff6-117">There is no limit to the number of backup files that the service can create (limited only by available disk space).</span></span> <span data-ttu-id="76ff6-118">I nomi dei file di backup sono nel formato Archive-*ChannelName* - *timestamp*. evtx e si trovano nella cartella% windir% \\ system32 \\ winevt \\ logs.</span><span class="sxs-lookup"><span data-stu-id="76ff6-118">The backup file names are of the form Archive-*channelName*-*timestamp*.evtx and are located in %windir%\\System32\\winevt\\Logs folder.</span></span><br/> |
| [<span data-ttu-id="76ff6-119">**maxSize**</span><span class="sxs-lookup"><span data-stu-id="76ff6-119">**maxSize**</span></span>](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [<span data-ttu-id="76ff6-120">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="76ff6-120">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="76ff6-121">Dimensione massima, in byte, del file di log.</span><span class="sxs-lookup"><span data-stu-id="76ff6-121">The maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="76ff6-122">Il valore predefinito (e minimo) è 1 MB.</span><span class="sxs-lookup"><span data-stu-id="76ff6-122">The default (and minimum) value is 1 MB.</span></span> <span data-ttu-id="76ff6-123">Se le dimensioni del log fisico sono inferiori alle dimensioni massime configurate ed è necessario spazio aggiuntivo nel log per archiviare gli eventi, il servizio alloca un altro blocco di spazio anche se la dimensione fisica risultante del log sarà maggiore della dimensione massima configurata.</span><span class="sxs-lookup"><span data-stu-id="76ff6-123">If the physical log size is less than the configured maximum size and additional space is required in the log to store events, the service will allocate another block of space even if the resulting physical size of the log will be larger than the configured maximum size.</span></span> <span data-ttu-id="76ff6-124">Il servizio alloca blocchi di 1 MB in modo che le dimensioni fisiche possano raggiungere un massimo di 1 MB rispetto alla dimensione massima configurata.</span><span class="sxs-lookup"><span data-stu-id="76ff6-124">The service allocates blocks of 1 MB so the physical size could grow to up to 1 MB larger than the configured max size.</span></span> <br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="76ff6-125">**conservazione**</span><span class="sxs-lookup"><span data-stu-id="76ff6-125">**retention**</span></span>](eventmanifestschema-retention-channelloggingtype-element.md)   | <span data-ttu-id="76ff6-126">boolean</span><span class="sxs-lookup"><span data-stu-id="76ff6-126">boolean</span></span>                                                           | <span data-ttu-id="76ff6-127">Determina se il file di log è un file di log sequenziale o circolare.</span><span class="sxs-lookup"><span data-stu-id="76ff6-127">Determines whether the log file is a sequential or circular log file.</span></span> <span data-ttu-id="76ff6-128">Impostare su **true** per un file di log sequenziale e **false** per un file di log circolare.</span><span class="sxs-lookup"><span data-stu-id="76ff6-128">Set to **true** for a sequential log file and **false** for a circular log file.</span></span> <span data-ttu-id="76ff6-129">Il valore predefinito è **false** per i tipi di canale operativo e di amministrazione e **true** per i tipi di canale analitico e debug.</span><span class="sxs-lookup"><span data-stu-id="76ff6-129">The default is **false** for Admin and Operational channel types and **true** for Analytic and Debug channel types.</span></span><br/> <span data-ttu-id="76ff6-130">Per eseguire una query su un log circolare, è necessario innanzitutto disabilitare il canale.</span><span class="sxs-lookup"><span data-stu-id="76ff6-130">To query a circular log, you must first disable the channel.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="76ff6-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="76ff6-131">Remarks</span></span>

<span data-ttu-id="76ff6-132">È possibile specificare l'attributo **MaxSize** per qualsiasi tipo di canale.</span><span class="sxs-lookup"><span data-stu-id="76ff6-132">You can specify the **maxSize** attribute for any channel type.</span></span>

<span data-ttu-id="76ff6-133">È possibile specificare l'attributo **backup automatico** solo per i tipi di canale operativo e di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="76ff6-133">You can specify the **autoBackup** attribute only for Admin and Operational channel types.</span></span>

<span data-ttu-id="76ff6-134">È possibile impostare l'attributo di **conservazione** su false (registrazione circolare) per i tipi di canale operativo e di amministratore.</span><span class="sxs-lookup"><span data-stu-id="76ff6-134">You can set the **retention** attribute to false (circular logging) for Admin and Operational channel types.</span></span> <span data-ttu-id="76ff6-135">È possibile impostare l'attributo di **conservazione** su false (registrazione circolare) per i tipi di canale analitici e di debug, ma per visualizzare gli eventi nel Visualizzatore eventi di Windows, sarà necessario disabilitare prima il canale.</span><span class="sxs-lookup"><span data-stu-id="76ff6-135">You can set the **retention** attribute to false (circular logging) for Analytic and Debug channel types but to view the events in the Windows Event Viewer, you will need to first disable the channel.</span></span> <span data-ttu-id="76ff6-136">Si noti che quando si Abilita nuovamente il canale, gli eventi vengono rimossi dal canale.</span><span class="sxs-lookup"><span data-stu-id="76ff6-136">Note that when you enable the channel again, the events are removed from the channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ff6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76ff6-137">Requirements</span></span>



| <span data-ttu-id="76ff6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ff6-138">Requirement</span></span> | <span data-ttu-id="76ff6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="76ff6-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76ff6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ff6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="76ff6-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76ff6-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76ff6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ff6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="76ff6-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76ff6-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





