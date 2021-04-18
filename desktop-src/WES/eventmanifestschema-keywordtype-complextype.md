---
title: Tipo complesso KeywordType
description: Definisce una parola chiave che identifica una categoria di eventi. | Tipo complesso KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Log eventi di tipo complesso KeywordType
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321529"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="f0277-105">Tipo complesso KeywordType</span><span class="sxs-lookup"><span data-stu-id="f0277-105">KeywordType Complex Type</span></span>

<span data-ttu-id="f0277-106">Definisce una parola chiave che identifica una categoria di eventi.</span><span class="sxs-lookup"><span data-stu-id="f0277-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="f0277-107">Una parola chiave è un tag che viene collegato a un evento per raggruppare gli eventi in base al relativo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="f0277-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="f0277-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="f0277-108">Attributes</span></span>



| <span data-ttu-id="f0277-109">Nome</span><span class="sxs-lookup"><span data-stu-id="f0277-109">Name</span></span>    | <span data-ttu-id="f0277-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0277-110">Type</span></span>                                                              | <span data-ttu-id="f0277-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0277-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0277-112">mask</span><span class="sxs-lookup"><span data-stu-id="f0277-112">mask</span></span>    | [<span data-ttu-id="f0277-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="f0277-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="f0277-114">Maschera di bit che deve avere solo un set di bit singolo.</span><span class="sxs-lookup"><span data-stu-id="f0277-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="f0277-115">Il bit rappresenta una categoria di eventi, ad esempio gli eventi di lettura o di scrittura.</span><span class="sxs-lookup"><span data-stu-id="f0277-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="f0277-116">È possibile specificare i valori di bit nell'intervallo compreso tra 0x0000000000000001 e 0x0000800000000000 (bit da 0 a 47).</span><span class="sxs-lookup"><span data-stu-id="f0277-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="f0277-117">message</span><span class="sxs-lookup"><span data-stu-id="f0277-117">message</span></span> | [<span data-ttu-id="f0277-118">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="f0277-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="f0277-119">Nome visualizzato localizzato per la parola chiave.</span><span class="sxs-lookup"><span data-stu-id="f0277-119">The localized display name for the keyword.</span></span> <span data-ttu-id="f0277-120">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="f0277-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="f0277-121">name</span><span class="sxs-lookup"><span data-stu-id="f0277-121">name</span></span>    | <span data-ttu-id="f0277-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="f0277-122">**QName**</span></span>                                                         | <span data-ttu-id="f0277-123">Nome della parola chiave.</span><span class="sxs-lookup"><span data-stu-id="f0277-123">The name of the keyword.</span></span> <span data-ttu-id="f0277-124">Il nome deve essere univoco all'interno dell'elenco di parole chiave definite dal provider.</span><span class="sxs-lookup"><span data-stu-id="f0277-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="f0277-125">simbolo</span><span class="sxs-lookup"><span data-stu-id="f0277-125">symbol</span></span>  | [<span data-ttu-id="f0277-126">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="f0277-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="f0277-127">Simbolo da utilizzare per fare riferimento alla parola chiave nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0277-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="f0277-128">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la parola chiave nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="f0277-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="f0277-129">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f0277-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0277-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0277-130">Remarks</span></span>

<span data-ttu-id="f0277-131">Il file Winmeta.xml incluso nell'Windows SDK contiene un elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="f0277-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="f0277-132">Queste parole chiave sono riservate e non devono essere usate.</span><span class="sxs-lookup"><span data-stu-id="f0277-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0277-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0277-133">Requirements</span></span>



| <span data-ttu-id="f0277-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0277-134">Requirement</span></span> | <span data-ttu-id="f0277-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f0277-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0277-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0277-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f0277-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0277-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0277-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0277-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f0277-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f0277-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





