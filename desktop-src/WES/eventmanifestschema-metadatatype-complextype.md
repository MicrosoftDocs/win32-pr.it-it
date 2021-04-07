---
title: Tipo complesso MetadataType
description: Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Log eventi di tipo complesso MetadataType
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048721"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="0f3db-104">Tipo complesso MetadataType</span><span class="sxs-lookup"><span data-stu-id="0f3db-104">MetadataType Complex Type</span></span>

<span data-ttu-id="0f3db-105">Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.</span><span class="sxs-lookup"><span data-stu-id="0f3db-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0f3db-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0f3db-106">Child elements</span></span>



| <span data-ttu-id="0f3db-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f3db-107">Element</span></span>                                                                       | <span data-ttu-id="0f3db-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f3db-108">Type</span></span>                                                                       | <span data-ttu-id="0f3db-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f3db-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f3db-110">**canali**</span><span class="sxs-lookup"><span data-stu-id="0f3db-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="0f3db-111">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="0f3db-112">Definisce un elenco di canali a cui i provider possono registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0f3db-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="0f3db-113">Un provider può quindi importare uno o più canali nel relativo manifesto.</span><span class="sxs-lookup"><span data-stu-id="0f3db-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="0f3db-114">**Parole**</span><span class="sxs-lookup"><span data-stu-id="0f3db-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="0f3db-115">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="0f3db-116">Definisce un elenco di parole chiave che determinano la categoria di eventi scritti dal provider.</span><span class="sxs-lookup"><span data-stu-id="0f3db-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="0f3db-117">**livelli**</span><span class="sxs-lookup"><span data-stu-id="0f3db-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="0f3db-118">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="0f3db-119">Definisce un elenco di livelli che specificano la gravità di un evento.</span><span class="sxs-lookup"><span data-stu-id="0f3db-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="0f3db-120">**message**</span><span class="sxs-lookup"><span data-stu-id="0f3db-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="0f3db-121">Definisce una stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0f3db-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="0f3db-122">**messageTable**</span><span class="sxs-lookup"><span data-stu-id="0f3db-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="0f3db-123">Definisce un elenco di stringhe di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0f3db-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="0f3db-124">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="0f3db-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="0f3db-125">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="0f3db-126">Definisce un elenco di query denominate che utilizzano espressioni regolari per eseguire operazioni di ricerca e sostituzione sulla stringa di messaggio di un evento.</span><span class="sxs-lookup"><span data-stu-id="0f3db-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="0f3db-127">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="0f3db-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="0f3db-128">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="0f3db-129">Definisce un elenco di codici operativi che è possibile usare per raggruppare gli eventi all'interno di un'attività.</span><span class="sxs-lookup"><span data-stu-id="0f3db-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="0f3db-130">**attività**</span><span class="sxs-lookup"><span data-stu-id="0f3db-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="0f3db-131">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="0f3db-132">Definisce un elenco di attività che possono essere utilizzate da un provider per raggruppare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="0f3db-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="0f3db-133">In genere, è possibile utilizzare le attività per raggruppare gli eventi per una funzionalità o un componente del provider.</span><span class="sxs-lookup"><span data-stu-id="0f3db-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="0f3db-134">**tipi**</span><span class="sxs-lookup"><span data-stu-id="0f3db-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="0f3db-135">**TypeListType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="0f3db-136">Definisce un elenco di tipi XML.</span><span class="sxs-lookup"><span data-stu-id="0f3db-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="0f3db-137">Attributi</span><span class="sxs-lookup"><span data-stu-id="0f3db-137">Attributes</span></span>



| <span data-ttu-id="0f3db-138">Nome</span><span class="sxs-lookup"><span data-stu-id="0f3db-138">Name</span></span>    | <span data-ttu-id="0f3db-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f3db-139">Type</span></span>                                                              | <span data-ttu-id="0f3db-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f3db-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3db-141">message</span><span class="sxs-lookup"><span data-stu-id="0f3db-141">message</span></span> | [<span data-ttu-id="0f3db-142">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="0f3db-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="0f3db-143">Riferimento alla stringa localizzata nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="0f3db-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="0f3db-144">mid</span><span class="sxs-lookup"><span data-stu-id="0f3db-144">mid</span></span>     | <span data-ttu-id="0f3db-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f3db-145">xs:string</span></span>                                                         | <span data-ttu-id="0f3db-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0f3db-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="0f3db-147">name</span><span class="sxs-lookup"><span data-stu-id="0f3db-147">name</span></span>    | <span data-ttu-id="0f3db-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="0f3db-148">anyURI</span></span>                                                            | <span data-ttu-id="0f3db-149">URI del file meta.</span><span class="sxs-lookup"><span data-stu-id="0f3db-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="0f3db-150">simbolo</span><span class="sxs-lookup"><span data-stu-id="0f3db-150">symbol</span></span>  | [<span data-ttu-id="0f3db-151">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="0f3db-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="0f3db-152">Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="0f3db-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="0f3db-153">Valore</span><span class="sxs-lookup"><span data-stu-id="0f3db-153">value</span></span>   | [<span data-ttu-id="0f3db-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="0f3db-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="0f3db-155">Numero da utilizzare come identificatore del messaggio per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0f3db-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="0f3db-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f3db-156">Remarks</span></span>

<span data-ttu-id="0f3db-157">Sebbene sia possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo utilizzerà. gli unici metadati riconosciuti dal servizio sono i metadati trovati nel file di Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="0f3db-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3db-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f3db-158">Requirements</span></span>



| <span data-ttu-id="0f3db-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f3db-159">Requirement</span></span> | <span data-ttu-id="0f3db-160">Valore</span><span class="sxs-lookup"><span data-stu-id="0f3db-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f3db-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f3db-161">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3db-162">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f3db-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f3db-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f3db-163">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3db-164">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f3db-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





