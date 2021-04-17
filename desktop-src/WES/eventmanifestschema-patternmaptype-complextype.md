---
title: Tipo complesso PatternMapType
description: Non usato. Definisce un mapping tra due espressioni regolari. Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- Log eventi di tipo complesso PatternMapType
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477392"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="cf0f6-106">Tipo complesso PatternMapType</span><span class="sxs-lookup"><span data-stu-id="cf0f6-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="cf0f6-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-107">Not used.</span></span> <span data-ttu-id="cf0f6-108">Definisce un mapping tra due espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="cf0f6-109">Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cf0f6-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cf0f6-110">Child elements</span></span>



| <span data-ttu-id="cf0f6-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf0f6-111">Element</span></span>                                                       | <span data-ttu-id="cf0f6-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0f6-112">Type</span></span>                                                                               | <span data-ttu-id="cf0f6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf0f6-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf0f6-114">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="cf0f6-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="cf0f6-115">**PatternMapValueType**</span><span class="sxs-lookup"><span data-stu-id="cf0f6-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="cf0f6-116">Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="cf0f6-117">Attributi</span><span class="sxs-lookup"><span data-stu-id="cf0f6-117">Attributes</span></span>



| <span data-ttu-id="cf0f6-118">Nome</span><span class="sxs-lookup"><span data-stu-id="cf0f6-118">Name</span></span>   | <span data-ttu-id="cf0f6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0f6-119">Type</span></span>                                                              | <span data-ttu-id="cf0f6-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf0f6-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0f6-121">format</span><span class="sxs-lookup"><span data-stu-id="cf0f6-121">format</span></span> | <span data-ttu-id="cf0f6-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="cf0f6-122">anyURI</span></span>                                                            | <span data-ttu-id="cf0f6-123">Motore delle espressioni regolari da usare.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cf0f6-124">name</span><span class="sxs-lookup"><span data-stu-id="cf0f6-124">name</span></span>   | <span data-ttu-id="cf0f6-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="cf0f6-125">**QName**</span></span>                                                         | <span data-ttu-id="cf0f6-126">Nome della mappa del pattern.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-126">The name of the pattern map.</span></span> <span data-ttu-id="cf0f6-127">Utilizzare il nome in un elemento dati per fare riferimento ai mapping.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="cf0f6-128">simbolo</span><span class="sxs-lookup"><span data-stu-id="cf0f6-128">symbol</span></span> | [<span data-ttu-id="cf0f6-129">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="cf0f6-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="cf0f6-130">Simbolo da utilizzare per fare riferimento ai mapping nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="cf0f6-131">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="cf0f6-132">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cf0f6-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cf0f6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf0f6-133">Requirements</span></span>



| <span data-ttu-id="cf0f6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf0f6-134">Requirement</span></span> | <span data-ttu-id="cf0f6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="cf0f6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf0f6-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf0f6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0f6-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf0f6-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf0f6-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf0f6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0f6-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf0f6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





