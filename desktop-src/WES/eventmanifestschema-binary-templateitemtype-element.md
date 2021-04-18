---
title: Binary (TemplateItemType)-elemento
description: Contiene i dati binari forniti dall'API del registro eventi.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- EventLog elemento binario
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302336"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="251a8-104">Binary (TemplateItemType)-elemento</span><span class="sxs-lookup"><span data-stu-id="251a8-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="251a8-105">Contiene i dati binari forniti dall'API del [registro eventi](/windows/desktop/EventLog/event-logging) .</span><span class="sxs-lookup"><span data-stu-id="251a8-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="251a8-106">L'elemento **binario** è definito dal tipo complesso [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="251a8-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="251a8-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="251a8-107">Attributes</span></span>



| <span data-ttu-id="251a8-108">Nome</span><span class="sxs-lookup"><span data-stu-id="251a8-108">Name</span></span> | <span data-ttu-id="251a8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="251a8-109">Type</span></span>   | <span data-ttu-id="251a8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="251a8-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="251a8-111">name</span><span class="sxs-lookup"><span data-stu-id="251a8-111">name</span></span> | <span data-ttu-id="251a8-112">string</span><span class="sxs-lookup"><span data-stu-id="251a8-112">string</span></span> | <span data-ttu-id="251a8-113">Nome associato ai dati binari.</span><span class="sxs-lookup"><span data-stu-id="251a8-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="251a8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="251a8-114">Requirements</span></span>



| <span data-ttu-id="251a8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="251a8-115">Requirement</span></span> | <span data-ttu-id="251a8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="251a8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="251a8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="251a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="251a8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="251a8-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="251a8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="251a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="251a8-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="251a8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="251a8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="251a8-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="251a8-122">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="251a8-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="251a8-123">**modello (TemplateListType)**</span><span class="sxs-lookup"><span data-stu-id="251a8-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

