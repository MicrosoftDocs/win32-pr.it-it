---
title: Tipo complesso DebugDataType
description: Definisce i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Log eventi di tipo complesso DebugDataType
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047789"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="a60ac-104">Tipo complesso DebugDataType</span><span class="sxs-lookup"><span data-stu-id="a60ac-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="a60ac-105">Definisce i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).</span><span class="sxs-lookup"><span data-stu-id="a60ac-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
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

## <a name="child-elements"></a><span data-ttu-id="a60ac-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a60ac-106">Child elements</span></span>



| <span data-ttu-id="a60ac-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a60ac-107">Element</span></span>                                                                    | <span data-ttu-id="a60ac-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a60ac-108">Type</span></span>        | <span data-ttu-id="a60ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a60ac-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a60ac-110">**Componente**</span><span class="sxs-lookup"><span data-stu-id="a60ac-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="a60ac-111">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-111">string</span></span>      | <span data-ttu-id="a60ac-112">Nome del componente che ha registrato il messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="a60ac-113">**FileLine**</span><span class="sxs-lookup"><span data-stu-id="a60ac-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="a60ac-114">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-114">string</span></span>      | <span data-ttu-id="a60ac-115">Il nome del file di origine e la riga all'interno del file di origine che ha registrato il messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="a60ac-116">**FlagName**</span><span class="sxs-lookup"><span data-stu-id="a60ac-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="a60ac-117">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-117">string</span></span>      | <span data-ttu-id="a60ac-118">Valore del flag passato al provider quando è stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="a60ac-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="a60ac-119">**Funzione**</span><span class="sxs-lookup"><span data-stu-id="a60ac-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="a60ac-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a60ac-120">unsignedInt</span></span> | <span data-ttu-id="a60ac-121">Nome della funzione che ha registrato il messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="a60ac-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="a60ac-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="a60ac-123">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-123">string</span></span>      | <span data-ttu-id="a60ac-124">Valore del livello passato al provider quando è stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="a60ac-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="a60ac-125">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="a60ac-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="a60ac-126">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-126">string</span></span>      | <span data-ttu-id="a60ac-127">La stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a60ac-127">The message string.</span></span> <span data-ttu-id="a60ac-128">Il codice XML contiene questo elemento se l'evento WPP ha specificato il campo FormattedString.</span><span class="sxs-lookup"><span data-stu-id="a60ac-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="a60ac-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="a60ac-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="a60ac-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a60ac-130">unsignedInt</span></span> | <span data-ttu-id="a60ac-131">Numero di sequenza locale o globale del messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="a60ac-132">**Sottocomponente**</span><span class="sxs-lookup"><span data-stu-id="a60ac-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="a60ac-133">string</span><span class="sxs-lookup"><span data-stu-id="a60ac-133">string</span></span>      | <span data-ttu-id="a60ac-134">Nome del sottocomponente che ha registrato il messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="a60ac-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="a60ac-135">Remarks</span></span>

<span data-ttu-id="a60ac-136">Gli elementi sono inclusi solo se il provider imposta la \_ \_ variabile di ambiente% Trace Format Prefix% per includerli.</span><span class="sxs-lookup"><span data-stu-id="a60ac-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="a60ac-137">Per informazioni dettagliate su questi elementi, vedere prefisso del messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="a60ac-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="a60ac-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a60ac-138">Requirements</span></span>



| <span data-ttu-id="a60ac-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a60ac-139">Requirement</span></span> | <span data-ttu-id="a60ac-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a60ac-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a60ac-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a60ac-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a60ac-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a60ac-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a60ac-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a60ac-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a60ac-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a60ac-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





