---
title: Tipo complesso XmlTypeListType
description: Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Log eventi di tipo complesso XmlTypeListType
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340793"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="43691-104">Tipo complesso XmlTypeListType</span><span class="sxs-lookup"><span data-stu-id="43691-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="43691-105">Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.</span><span class="sxs-lookup"><span data-stu-id="43691-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="43691-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="43691-106">Child elements</span></span>



| <span data-ttu-id="43691-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="43691-107">Element</span></span>                                                                | <span data-ttu-id="43691-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="43691-108">Type</span></span> | <span data-ttu-id="43691-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43691-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="43691-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="43691-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="43691-111">Definisce un tipo XML.</span><span class="sxs-lookup"><span data-stu-id="43691-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="43691-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="43691-112">Attributes</span></span>



| <span data-ttu-id="43691-113">Nome</span><span class="sxs-lookup"><span data-stu-id="43691-113">Name</span></span>   | <span data-ttu-id="43691-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="43691-114">Type</span></span>                                                              | <span data-ttu-id="43691-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43691-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43691-116">name</span><span class="sxs-lookup"><span data-stu-id="43691-116">name</span></span>   | <span data-ttu-id="43691-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="43691-117">**QName**</span></span>                                                         | <span data-ttu-id="43691-118">Nome del tipo di output.</span><span class="sxs-lookup"><span data-stu-id="43691-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="43691-119">simbolo</span><span class="sxs-lookup"><span data-stu-id="43691-119">symbol</span></span> | [<span data-ttu-id="43691-120">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="43691-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="43691-121">Simbolo da utilizzare per fare riferimento al tipo di output nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43691-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="43691-122">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il tipo di output nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="43691-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="43691-123">Valore</span><span class="sxs-lookup"><span data-stu-id="43691-123">value</span></span>  | <span data-ttu-id="43691-124">string</span><span class="sxs-lookup"><span data-stu-id="43691-124">string</span></span>                                                            | <span data-ttu-id="43691-125">Valore intero che identifica in modo univoco il tipo di output nell'elenco dei tipi di output definiti.</span><span class="sxs-lookup"><span data-stu-id="43691-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="43691-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="43691-126">Remarks</span></span>

<span data-ttu-id="43691-127">Il \\ \\ file di inclusioneWinmeta.xml, incluso nella Windows SDK, contiene un elenco di tipi di output predefiniti.</span><span class="sxs-lookup"><span data-stu-id="43691-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="43691-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43691-128">Requirements</span></span>



| <span data-ttu-id="43691-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="43691-129">Requirement</span></span> | <span data-ttu-id="43691-130">Valore</span><span class="sxs-lookup"><span data-stu-id="43691-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43691-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43691-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43691-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43691-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43691-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43691-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43691-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43691-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





