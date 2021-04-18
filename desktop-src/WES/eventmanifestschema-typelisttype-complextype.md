---
title: Tipo complesso TypeListType
description: Definisce i tipi utilizzati nel manifesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Log eventi di tipo complesso TypeListType
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302157"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="7362c-104">Tipo complesso TypeListType</span><span class="sxs-lookup"><span data-stu-id="7362c-104">TypeListType Complex Type</span></span>

<span data-ttu-id="7362c-105">Definisce i tipi utilizzati nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="7362c-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7362c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7362c-106">Child elements</span></span>



| <span data-ttu-id="7362c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7362c-107">Element</span></span>                                                               | <span data-ttu-id="7362c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7362c-108">Type</span></span>                                                                           | <span data-ttu-id="7362c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7362c-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7362c-110">**intipi**</span><span class="sxs-lookup"><span data-stu-id="7362c-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="7362c-111">**InputTypeListType**</span><span class="sxs-lookup"><span data-stu-id="7362c-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="7362c-112">Definisce un elenco di tipi di dati di input.</span><span class="sxs-lookup"><span data-stu-id="7362c-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="7362c-113">**xmltypes**</span><span class="sxs-lookup"><span data-stu-id="7362c-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="7362c-114">**XmlTypeListType**</span><span class="sxs-lookup"><span data-stu-id="7362c-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="7362c-115">Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.</span><span class="sxs-lookup"><span data-stu-id="7362c-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7362c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7362c-116">Requirements</span></span>



| <span data-ttu-id="7362c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7362c-117">Requirement</span></span> | <span data-ttu-id="7362c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7362c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7362c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7362c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7362c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7362c-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7362c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7362c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7362c-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7362c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





