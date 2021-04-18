---
title: Tipo complesso ComplexDataType
description: Definisce una struttura che contiene uno o più elementi di dati.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- Log eventi di tipo complesso ComplexDataType
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302156"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="7266a-104">Tipo complesso ComplexDataType</span><span class="sxs-lookup"><span data-stu-id="7266a-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="7266a-105">Definisce una struttura che contiene uno o più elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="7266a-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7266a-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7266a-106">Child elements</span></span>



| <span data-ttu-id="7266a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7266a-107">Element</span></span>                                                  | <span data-ttu-id="7266a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7266a-108">Type</span></span>                                                      | <span data-ttu-id="7266a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7266a-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7266a-110">**Data**</span><span class="sxs-lookup"><span data-stu-id="7266a-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="7266a-111">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7266a-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="7266a-112">Elenco di elementi di dati nella struttura.</span><span class="sxs-lookup"><span data-stu-id="7266a-112">The list of data items in the structure.</span></span> <span data-ttu-id="7266a-113">L'elenco di elementi è nello stesso ordine definito nel modello.</span><span class="sxs-lookup"><span data-stu-id="7266a-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="7266a-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="7266a-114">Attributes</span></span>



| <span data-ttu-id="7266a-115">Nome</span><span class="sxs-lookup"><span data-stu-id="7266a-115">Name</span></span> | <span data-ttu-id="7266a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="7266a-116">Type</span></span>   | <span data-ttu-id="7266a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7266a-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7266a-118">Nome</span><span class="sxs-lookup"><span data-stu-id="7266a-118">Name</span></span> | <span data-ttu-id="7266a-119">stringa</span><span class="sxs-lookup"><span data-stu-id="7266a-119">string</span></span> | <span data-ttu-id="7266a-120">Nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="7266a-120">The name of the structure.</span></span> <span data-ttu-id="7266a-121">Si tratta del nome specificato quando è stata definita la struttura nel modello (vedere il tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="7266a-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7266a-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7266a-122">Remarks</span></span>

<span data-ttu-id="7266a-123">La funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) esegue il rendering del contenuto di una struttura come BLOB binario; la funzione non esegue il rendering dei singoli elementi di dati della struttura.</span><span class="sxs-lookup"><span data-stu-id="7266a-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7266a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7266a-124">Requirements</span></span>



| <span data-ttu-id="7266a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7266a-125">Requirement</span></span> | <span data-ttu-id="7266a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7266a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7266a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7266a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7266a-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7266a-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7266a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7266a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7266a-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7266a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





