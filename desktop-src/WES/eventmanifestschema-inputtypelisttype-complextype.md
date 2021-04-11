---
title: Tipo complesso InputTypeListType
description: Definisce un elenco di tipi di input.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Log eventi di tipo complesso InputTypeListType
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121342"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="24b29-104">Tipo complesso InputTypeListType</span><span class="sxs-lookup"><span data-stu-id="24b29-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="24b29-105">Definisce un elenco di tipi di input.</span><span class="sxs-lookup"><span data-stu-id="24b29-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="24b29-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="24b29-106">Child elements</span></span>



| <span data-ttu-id="24b29-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="24b29-107">Element</span></span>                                                                | <span data-ttu-id="24b29-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="24b29-108">Type</span></span>                                                           | <span data-ttu-id="24b29-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24b29-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="24b29-110">**inType**</span><span class="sxs-lookup"><span data-stu-id="24b29-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="24b29-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="24b29-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="24b29-112">Definisce un tipo di input.</span><span class="sxs-lookup"><span data-stu-id="24b29-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="24b29-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b29-113">Requirements</span></span>



| <span data-ttu-id="24b29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b29-114">Requirement</span></span> | <span data-ttu-id="24b29-115">Valore</span><span class="sxs-lookup"><span data-stu-id="24b29-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24b29-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24b29-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24b29-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24b29-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24b29-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24b29-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





