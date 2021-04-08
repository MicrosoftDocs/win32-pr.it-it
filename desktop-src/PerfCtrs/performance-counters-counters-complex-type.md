---
description: Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori che forniscono.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipi complessi di contatori
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967507"
---
# <a name="counters-complex-type"></a><span data-ttu-id="de4ff-103">Tipi complessi di contatori</span><span class="sxs-lookup"><span data-stu-id="de4ff-103">counters Complex Type</span></span>

<span data-ttu-id="de4ff-104">Definisce la sezione del manifesto di strumentazione che identifica il provider e i contatori che forniscono.</span><span class="sxs-lookup"><span data-stu-id="de4ff-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="de4ff-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="de4ff-105">Child elements</span></span>



| <span data-ttu-id="de4ff-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="de4ff-106">Element</span></span>      | <span data-ttu-id="de4ff-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="de4ff-107">Type</span></span>                                                               | <span data-ttu-id="de4ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de4ff-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="de4ff-109">**provider**</span><span class="sxs-lookup"><span data-stu-id="de4ff-109">**provider**</span></span> | [<span data-ttu-id="de4ff-110">**uomo: provider**</span><span class="sxs-lookup"><span data-stu-id="de4ff-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="de4ff-111">Identifica un provider che fornisce contatori.</span><span class="sxs-lookup"><span data-stu-id="de4ff-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="de4ff-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="de4ff-112">Attributes</span></span>



| <span data-ttu-id="de4ff-113">Nome</span><span class="sxs-lookup"><span data-stu-id="de4ff-113">Name</span></span>          | <span data-ttu-id="de4ff-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="de4ff-114">Type</span></span> | <span data-ttu-id="de4ff-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de4ff-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="de4ff-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="de4ff-116">schemaVersion</span></span> |      | <span data-ttu-id="de4ff-117">Versione dello schema utilizzata per scrivere il manifesto.</span><span class="sxs-lookup"><span data-stu-id="de4ff-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="de4ff-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de4ff-118">Requirements</span></span>



| <span data-ttu-id="de4ff-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de4ff-119">Requirement</span></span> | <span data-ttu-id="de4ff-120">Valore</span><span class="sxs-lookup"><span data-stu-id="de4ff-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de4ff-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de4ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de4ff-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de4ff-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de4ff-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de4ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de4ff-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de4ff-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de4ff-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de4ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4ff-126">**Strumentazione**</span><span class="sxs-lookup"><span data-stu-id="de4ff-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

