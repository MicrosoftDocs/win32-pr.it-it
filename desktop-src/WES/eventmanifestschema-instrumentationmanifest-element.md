---
title: Elemento instrumentationManifest
description: Nodo radice del manifesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- EventLog elemento instrumentationManifest
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104234591"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="580e4-104">Elemento instrumentationManifest</span><span class="sxs-lookup"><span data-stu-id="580e4-104">instrumentationManifest Element</span></span>

<span data-ttu-id="580e4-105">Nodo radice del manifesto.</span><span class="sxs-lookup"><span data-stu-id="580e4-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="580e4-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="580e4-106">Child elements</span></span>



| <span data-ttu-id="580e4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="580e4-107">Element</span></span>                                                                                        | <span data-ttu-id="580e4-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="580e4-108">Type</span></span>                                                                               | <span data-ttu-id="580e4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="580e4-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="580e4-110">**Strumentazione**</span><span class="sxs-lookup"><span data-stu-id="580e4-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="580e4-111">**InstrumentationType**</span><span class="sxs-lookup"><span data-stu-id="580e4-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="580e4-112">Questa sezione definisce uno o più provider di eventi e gli eventi registrati.</span><span class="sxs-lookup"><span data-stu-id="580e4-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="580e4-113">**localizzazione**</span><span class="sxs-lookup"><span data-stu-id="580e4-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="580e4-114">**LocalizationType**</span><span class="sxs-lookup"><span data-stu-id="580e4-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="580e4-115">In questa sezione vengono definite le stringhe di messaggio localizzate utilizzate dai consumer per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="580e4-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="580e4-116">Questa sezione, ad esempio, contiene la stringa di messaggio localizzata per il nome del provider, gli eventi definiti ed eventuali attributi di evento definiti, ad esempio canali, attività e codici operativi.</span><span class="sxs-lookup"><span data-stu-id="580e4-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="580e4-117">**metadati**</span><span class="sxs-lookup"><span data-stu-id="580e4-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="580e4-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="580e4-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="580e4-119">Questa sezione definisce i tipi di metadati che possono essere usati da altri manifesti.</span><span class="sxs-lookup"><span data-stu-id="580e4-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="580e4-120">Per un esempio, vedere il file Winmeta.xml incluso nella \\ cartella di inclusione del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="580e4-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="580e4-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="580e4-121">Remarks</span></span>

<span data-ttu-id="580e4-122">L'elemento **instrumentationManifest** deve contenere gli spazi dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="580e4-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="580e4-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="580e4-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="580e4-124">xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="580e4-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="580e4-125">xmlns: XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="580e4-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="580e4-126">Un manifesto deve contenere una sezione di strumentazione e una sezione di localizzazione.</span><span class="sxs-lookup"><span data-stu-id="580e4-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="580e4-127">La sezione di strumentazione e la sezione dei metadati si escludono a vicenda (non è possibile definire entrambi nello stesso manifesto).</span><span class="sxs-lookup"><span data-stu-id="580e4-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="580e4-128">Sebbene sia possibile creare un manifesto che contiene una sezione di metadati, il servizio non lo utilizzerà. gli unici metadati riconosciuti dal servizio sono i metadati trovati nel file di Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="580e4-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="580e4-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="580e4-129">Examples</span></span>

<span data-ttu-id="580e4-130">Nell'esempio seguente viene illustrata la struttura di un manifesto di strumentazione completamente definito.</span><span class="sxs-lookup"><span data-stu-id="580e4-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="580e4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="580e4-131">Requirements</span></span>



| <span data-ttu-id="580e4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="580e4-132">Requirement</span></span> | <span data-ttu-id="580e4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="580e4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="580e4-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580e4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="580e4-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="580e4-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="580e4-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580e4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="580e4-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="580e4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





