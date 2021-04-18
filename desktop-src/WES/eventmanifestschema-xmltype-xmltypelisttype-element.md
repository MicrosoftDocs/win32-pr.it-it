---
title: Elemento XMLType (XmlTypeListType)
description: Definisce un tipo XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- XMLType-elemento EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301550"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="9e910-104">Elemento XMLType (XmlTypeListType)</span><span class="sxs-lookup"><span data-stu-id="9e910-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="9e910-105">Definisce un tipo XML.</span><span class="sxs-lookup"><span data-stu-id="9e910-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
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
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="9e910-106">L'elemento **XmlType** è definito dal tipo complesso [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9e910-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="9e910-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="9e910-107">Attributes</span></span>



| <span data-ttu-id="9e910-108">Nome</span><span class="sxs-lookup"><span data-stu-id="9e910-108">Name</span></span>   | <span data-ttu-id="9e910-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e910-109">Type</span></span>      | <span data-ttu-id="9e910-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e910-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e910-111">name</span><span class="sxs-lookup"><span data-stu-id="9e910-111">name</span></span>   | <span data-ttu-id="9e910-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="9e910-112">**QName**</span></span> | <span data-ttu-id="9e910-113">Nome del tipo di output.</span><span class="sxs-lookup"><span data-stu-id="9e910-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="9e910-114">simbolo</span><span class="sxs-lookup"><span data-stu-id="9e910-114">symbol</span></span> | <span data-ttu-id="9e910-115">string</span><span class="sxs-lookup"><span data-stu-id="9e910-115">string</span></span>    | <span data-ttu-id="9e910-116">Simbolo da utilizzare per fare riferimento al tipo di output nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e910-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="9e910-117">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il tipo di output nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="9e910-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="9e910-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9e910-118">value</span></span>  | <span data-ttu-id="9e910-119">string</span><span class="sxs-lookup"><span data-stu-id="9e910-119">string</span></span>    | <span data-ttu-id="9e910-120">Valore intero che identifica in modo univoco il tipo di output nell'elenco dei tipi di output definiti.</span><span class="sxs-lookup"><span data-stu-id="9e910-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="9e910-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e910-121">Requirements</span></span>



| <span data-ttu-id="9e910-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e910-122">Requirement</span></span> | <span data-ttu-id="9e910-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9e910-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e910-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e910-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e910-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e910-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e910-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e910-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e910-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e910-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e910-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e910-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e910-129">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="9e910-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9e910-130">**xmltypes (TypeListType)**</span><span class="sxs-lookup"><span data-stu-id="9e910-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





