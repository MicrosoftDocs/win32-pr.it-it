---
title: Tipo complesso ValueMapValueType
description: Definisce il mapping tra un valore integer e un valore stringa. | Tipo complesso ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- Log eventi di tipo complesso ValueMapValueType
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401856"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="a8735-105">Tipo complesso ValueMapValueType</span><span class="sxs-lookup"><span data-stu-id="a8735-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="a8735-106">Definisce il mapping tra un valore integer e un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="a8735-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="a8735-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a8735-107">Attributes</span></span>



| <span data-ttu-id="a8735-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a8735-108">Name</span></span>    | <span data-ttu-id="a8735-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8735-109">Type</span></span>                                                              | <span data-ttu-id="a8735-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8735-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8735-111">message</span><span class="sxs-lookup"><span data-stu-id="a8735-111">message</span></span> | [<span data-ttu-id="a8735-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="a8735-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a8735-113">Valore stringa localizzato a cui viene eseguito il mapping del valore intero.</span><span class="sxs-lookup"><span data-stu-id="a8735-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="a8735-114">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="a8735-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="a8735-115">simbolo</span><span class="sxs-lookup"><span data-stu-id="a8735-115">symbol</span></span>  | [<span data-ttu-id="a8735-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="a8735-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a8735-117">Simbolo da utilizzare per fare riferimento alla mappa nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8735-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="a8735-118">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="a8735-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="a8735-119">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a8735-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="a8735-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a8735-120">value</span></span>   | [<span data-ttu-id="a8735-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="a8735-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="a8735-122">Valore intero di cui eseguire il mapping al valore stringa.</span><span class="sxs-lookup"><span data-stu-id="a8735-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="a8735-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8735-123">Requirements</span></span>



| <span data-ttu-id="a8735-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8735-124">Requirement</span></span> | <span data-ttu-id="a8735-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a8735-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8735-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8735-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a8735-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8735-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8735-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8735-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a8735-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8735-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





