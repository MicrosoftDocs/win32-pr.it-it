---
title: Tipo complesso DataType (registro eventi di Windows)
description: Definisce un elemento di dati.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- Log eventi di tipo complesso DataType
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341053"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="b3d9e-104">Tipo complesso DataType</span><span class="sxs-lookup"><span data-stu-id="b3d9e-104">DataType Complex Type</span></span>

<span data-ttu-id="b3d9e-105">Definisce un elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="b3d9e-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b3d9e-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="b3d9e-106">Attributes</span></span>



| <span data-ttu-id="b3d9e-107">Nome</span><span class="sxs-lookup"><span data-stu-id="b3d9e-107">Name</span></span> | <span data-ttu-id="b3d9e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3d9e-108">Type</span></span>   | <span data-ttu-id="b3d9e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3d9e-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d9e-110">Nome</span><span class="sxs-lookup"><span data-stu-id="b3d9e-110">Name</span></span> | <span data-ttu-id="b3d9e-111">stringa</span><span class="sxs-lookup"><span data-stu-id="b3d9e-111">string</span></span> | <span data-ttu-id="b3d9e-112">Nome di un elemento di dati definito nel modello (vedere il tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="b3d9e-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="b3d9e-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3d9e-113">Type</span></span> | <span data-ttu-id="b3d9e-114">QName</span><span class="sxs-lookup"><span data-stu-id="b3d9e-114">QName</span></span>  | <span data-ttu-id="b3d9e-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b3d9e-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="b3d9e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3d9e-116">Remarks</span></span>

<span data-ttu-id="b3d9e-117">L'elemento dati può essere un elemento di dati di primo livello o un elemento dati in una struttura.</span><span class="sxs-lookup"><span data-stu-id="b3d9e-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d9e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3d9e-118">Requirements</span></span>



| <span data-ttu-id="b3d9e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d9e-119">Requirement</span></span> | <span data-ttu-id="b3d9e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b3d9e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3d9e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3d9e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d9e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3d9e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3d9e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3d9e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d9e-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3d9e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





