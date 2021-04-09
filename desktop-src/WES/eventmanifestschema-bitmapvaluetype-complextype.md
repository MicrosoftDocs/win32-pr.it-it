---
title: Tipo complesso BitMapValueType
description: Definisce il mapping tra un valore di bit e un valore stringa. | Tipo complesso BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Log eventi di tipo complesso BitMapValueType
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969150"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="a4dae-105">Tipo complesso BitMapValueType</span><span class="sxs-lookup"><span data-stu-id="a4dae-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="a4dae-106">Definisce il mapping tra un valore di bit e un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="a4dae-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="a4dae-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a4dae-107">Attributes</span></span>



| <span data-ttu-id="a4dae-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a4dae-108">Name</span></span>    | <span data-ttu-id="a4dae-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4dae-109">Type</span></span>                                                              | <span data-ttu-id="a4dae-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4dae-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4dae-111">message</span><span class="sxs-lookup"><span data-stu-id="a4dae-111">message</span></span> | [<span data-ttu-id="a4dae-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="a4dae-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a4dae-113">Valore stringa localizzato a cui viene eseguito il mapping del valore di bit.</span><span class="sxs-lookup"><span data-stu-id="a4dae-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="a4dae-114">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="a4dae-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="a4dae-115">simbolo</span><span class="sxs-lookup"><span data-stu-id="a4dae-115">symbol</span></span>  | [<span data-ttu-id="a4dae-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="a4dae-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a4dae-117">Simbolo da utilizzare per fare riferimento alla mappa nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4dae-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="a4dae-118">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="a4dae-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="a4dae-119">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a4dae-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="a4dae-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a4dae-120">value</span></span>   | [<span data-ttu-id="a4dae-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="a4dae-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="a4dae-122">Valore di bit di cui eseguire il mapping al valore stringa.</span><span class="sxs-lookup"><span data-stu-id="a4dae-122">The bit value to map to the string value.</span></span> <span data-ttu-id="a4dae-123">È necessario specificare un numero esadecimale con un singolo set di bit.</span><span class="sxs-lookup"><span data-stu-id="a4dae-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a4dae-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4dae-124">Remarks</span></span>

<span data-ttu-id="a4dae-125">Esegue il mapping di un valore esadecimale (il numero deve essere preceduto da 0x) con un solo bit impostato su un nome.</span><span class="sxs-lookup"><span data-stu-id="a4dae-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4dae-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4dae-126">Requirements</span></span>



| <span data-ttu-id="a4dae-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4dae-127">Requirement</span></span> | <span data-ttu-id="a4dae-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a4dae-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4dae-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4dae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a4dae-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4dae-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4dae-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4dae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a4dae-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4dae-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





