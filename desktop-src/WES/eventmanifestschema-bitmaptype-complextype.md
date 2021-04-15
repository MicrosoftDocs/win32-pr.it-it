---
title: Tipo complesso BitMapType
description: Definisce un elenco di mapping nome/valore tra valori di bit e valori di stringa.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- Log eventi di tipo complesso BitMapType
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479216"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="80d31-104">Tipo complesso BitMapType</span><span class="sxs-lookup"><span data-stu-id="80d31-104">BitMapType Complex Type</span></span>

<span data-ttu-id="80d31-105">Definisce un elenco di mapping nome/valore tra valori di bit e valori di stringa.</span><span class="sxs-lookup"><span data-stu-id="80d31-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="80d31-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="80d31-106">Child elements</span></span>



| <span data-ttu-id="80d31-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="80d31-107">Element</span></span>                                                   | <span data-ttu-id="80d31-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="80d31-108">Type</span></span>                                                                       | <span data-ttu-id="80d31-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d31-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="80d31-110">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="80d31-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="80d31-111">**BitMapValueType**</span><span class="sxs-lookup"><span data-stu-id="80d31-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="80d31-112">Definisce il mapping tra un valore di bit e un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="80d31-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="80d31-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="80d31-113">Attributes</span></span>



| <span data-ttu-id="80d31-114">Nome</span><span class="sxs-lookup"><span data-stu-id="80d31-114">Name</span></span>   | <span data-ttu-id="80d31-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="80d31-115">Type</span></span>                                                              | <span data-ttu-id="80d31-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d31-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d31-117">name</span><span class="sxs-lookup"><span data-stu-id="80d31-117">name</span></span>   | <span data-ttu-id="80d31-118">string</span><span class="sxs-lookup"><span data-stu-id="80d31-118">string</span></span>                                                            | <span data-ttu-id="80d31-119">Nome della bitmap.</span><span class="sxs-lookup"><span data-stu-id="80d31-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="80d31-120">simbolo</span><span class="sxs-lookup"><span data-stu-id="80d31-120">symbol</span></span> | [<span data-ttu-id="80d31-121">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="80d31-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="80d31-122">Simbolo da utilizzare per fare riferimento ai mapping nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80d31-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="80d31-123">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="80d31-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="80d31-124">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="80d31-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="80d31-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80d31-125">Requirements</span></span>



| <span data-ttu-id="80d31-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="80d31-126">Requirement</span></span> | <span data-ttu-id="80d31-127">Valore</span><span class="sxs-lookup"><span data-stu-id="80d31-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80d31-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80d31-128">Minimum supported client</span></span><br/> | <span data-ttu-id="80d31-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80d31-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80d31-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80d31-130">Minimum supported server</span></span><br/> | <span data-ttu-id="80d31-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80d31-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





