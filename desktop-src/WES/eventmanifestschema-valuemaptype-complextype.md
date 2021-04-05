---
title: Tipo complesso ValueMapType
description: Definisce un elenco di mapping nome/valore tra valori interi e valori di stringa.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- Log eventi di tipo complesso ValueMapType
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739714"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="4503c-104">Tipo complesso ValueMapType</span><span class="sxs-lookup"><span data-stu-id="4503c-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="4503c-105">Definisce un elenco di mapping nome/valore tra valori interi e valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="4503c-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4503c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4503c-106">Child elements</span></span>



| <span data-ttu-id="4503c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="4503c-107">Element</span></span>                                                     | <span data-ttu-id="4503c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4503c-108">Type</span></span>                                                                           | <span data-ttu-id="4503c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4503c-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="4503c-110">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="4503c-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="4503c-111">**ValueMapValueType**</span><span class="sxs-lookup"><span data-stu-id="4503c-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="4503c-112">Definisce il mapping tra un valore integer e un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="4503c-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4503c-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="4503c-113">Attributes</span></span>



| <span data-ttu-id="4503c-114">Nome</span><span class="sxs-lookup"><span data-stu-id="4503c-114">Name</span></span>   | <span data-ttu-id="4503c-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="4503c-115">Type</span></span>                                                              | <span data-ttu-id="4503c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4503c-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4503c-117">name</span><span class="sxs-lookup"><span data-stu-id="4503c-117">name</span></span>   | <span data-ttu-id="4503c-118">string</span><span class="sxs-lookup"><span data-stu-id="4503c-118">string</span></span>                                                            | <span data-ttu-id="4503c-119">Nome della mappa del valore.</span><span class="sxs-lookup"><span data-stu-id="4503c-119">The name of the value map.</span></span> <span data-ttu-id="4503c-120">Utilizzare il nome in un elemento dati per fare riferimento ai mapping.</span><span class="sxs-lookup"><span data-stu-id="4503c-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="4503c-121">simbolo</span><span class="sxs-lookup"><span data-stu-id="4503c-121">symbol</span></span> | [<span data-ttu-id="4503c-122">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="4503c-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="4503c-123">Simbolo da utilizzare per fare riferimento ai mapping nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4503c-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="4503c-124">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="4503c-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="4503c-125">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4503c-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4503c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4503c-126">Requirements</span></span>



| <span data-ttu-id="4503c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4503c-127">Requirement</span></span> | <span data-ttu-id="4503c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4503c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4503c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4503c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4503c-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4503c-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4503c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4503c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4503c-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4503c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





