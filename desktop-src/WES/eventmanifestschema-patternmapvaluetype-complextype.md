---
title: Tipo complesso PatternMapValueType
description: Non usato. Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- Log eventi di tipo complesso PatternMapValueType
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739730"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="0e007-105">Tipo complesso PatternMapValueType</span><span class="sxs-lookup"><span data-stu-id="0e007-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="0e007-106">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0e007-106">Not used.</span></span> <span data-ttu-id="0e007-107">Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.</span><span class="sxs-lookup"><span data-stu-id="0e007-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="0e007-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="0e007-108">Attributes</span></span>



| <span data-ttu-id="0e007-109">Nome</span><span class="sxs-lookup"><span data-stu-id="0e007-109">Name</span></span>  | <span data-ttu-id="0e007-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e007-110">Type</span></span>   | <span data-ttu-id="0e007-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e007-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e007-112">name</span><span class="sxs-lookup"><span data-stu-id="0e007-112">name</span></span>  | <span data-ttu-id="0e007-113">string</span><span class="sxs-lookup"><span data-stu-id="0e007-113">string</span></span> | <span data-ttu-id="0e007-114">Espressione regolare utilizzata per trovare una stringa corrispondente nella stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0e007-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="0e007-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e007-115">value</span></span> | <span data-ttu-id="0e007-116">string</span><span class="sxs-lookup"><span data-stu-id="0e007-116">string</span></span> | <span data-ttu-id="0e007-117">Espressione regolare utilizzata per modificare la stringa corrispondente trovata nella stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="0e007-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0e007-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e007-118">Requirements</span></span>



| <span data-ttu-id="0e007-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e007-119">Requirement</span></span> | <span data-ttu-id="0e007-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0e007-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e007-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e007-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e007-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e007-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e007-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e007-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e007-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e007-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





