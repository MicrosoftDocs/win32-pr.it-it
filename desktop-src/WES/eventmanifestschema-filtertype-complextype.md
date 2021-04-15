---
title: Tipo complesso FilterType
description: Definisce un filtro di dati utilizzato da una sessione per filtrare gli eventi in base ai dati dell'evento.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- Log eventi di tipo complesso FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479276"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="5e77f-104">Tipo complesso FilterType</span><span class="sxs-lookup"><span data-stu-id="5e77f-104">FilterType Complex Type</span></span>

<span data-ttu-id="5e77f-105">Definisce un filtro di dati utilizzato da una sessione per filtrare gli eventi in base ai dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5e77f-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="5e77f-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="5e77f-106">Attributes</span></span>



| <span data-ttu-id="5e77f-107">Nome</span><span class="sxs-lookup"><span data-stu-id="5e77f-107">Name</span></span>    | <span data-ttu-id="5e77f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e77f-108">Type</span></span>                                                              | <span data-ttu-id="5e77f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e77f-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e77f-110">message</span><span class="sxs-lookup"><span data-stu-id="5e77f-110">message</span></span> | [<span data-ttu-id="5e77f-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="5e77f-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="5e77f-112">Descrizione localizzata per il filtro.</span><span class="sxs-lookup"><span data-stu-id="5e77f-112">The localized description for the filter.</span></span> <span data-ttu-id="5e77f-113">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="5e77f-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="5e77f-114">name</span><span class="sxs-lookup"><span data-stu-id="5e77f-114">name</span></span>    | <span data-ttu-id="5e77f-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="5e77f-115">**QName**</span></span>                                                         | <span data-ttu-id="5e77f-116">Nome che identifica il filtro.</span><span class="sxs-lookup"><span data-stu-id="5e77f-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="5e77f-117">simbolo</span><span class="sxs-lookup"><span data-stu-id="5e77f-117">symbol</span></span>  | [<span data-ttu-id="5e77f-118">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="5e77f-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="5e77f-119">Simbolo da utilizzare per fare riferimento al filtro nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e77f-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="5e77f-120">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il filtro nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="5e77f-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="5e77f-121">tid</span><span class="sxs-lookup"><span data-stu-id="5e77f-121">tid</span></span>     | <span data-ttu-id="5e77f-122">token</span><span class="sxs-lookup"><span data-stu-id="5e77f-122">token</span></span>                                                             | <span data-ttu-id="5e77f-123">Identificatore di modello che descrive i dati del filtro che la sessione passa al provider quando Abilita il provider.</span><span class="sxs-lookup"><span data-stu-id="5e77f-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="5e77f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5e77f-124">value</span></span>   | [<span data-ttu-id="5e77f-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="5e77f-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="5e77f-126">Valore intero che identifica in modo univoco il filtro all'interno dell'elenco di filtri definiti.</span><span class="sxs-lookup"><span data-stu-id="5e77f-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="5e77f-127">version</span><span class="sxs-lookup"><span data-stu-id="5e77f-127">version</span></span> | [<span data-ttu-id="5e77f-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="5e77f-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="5e77f-129">Valore intero che identifica la versione del filtro.</span><span class="sxs-lookup"><span data-stu-id="5e77f-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="5e77f-130">Se non è specificato, il valore è zero.</span><span class="sxs-lookup"><span data-stu-id="5e77f-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="5e77f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e77f-131">Requirements</span></span>



| <span data-ttu-id="5e77f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e77f-132">Requirement</span></span> | <span data-ttu-id="5e77f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5e77f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5e77f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e77f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e77f-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5e77f-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5e77f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e77f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e77f-137">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e77f-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





