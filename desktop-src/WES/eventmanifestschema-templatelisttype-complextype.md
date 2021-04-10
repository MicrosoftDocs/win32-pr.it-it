---
title: Tipo complesso TemplateListType
description: Definisce un elenco di modelli che specificano i dati da includere con gli eventi. | Tipo complesso TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- Log eventi di tipo complesso TemplateListType
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761777"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="cc1a9-105">Tipo complesso TemplateListType</span><span class="sxs-lookup"><span data-stu-id="cc1a9-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="cc1a9-106">Definisce un elenco di modelli che specificano i dati da includere con gli eventi.</span><span class="sxs-lookup"><span data-stu-id="cc1a9-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cc1a9-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cc1a9-107">Child elements</span></span>



| <span data-ttu-id="cc1a9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc1a9-108">Element</span></span>                                                                   | <span data-ttu-id="cc1a9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc1a9-109">Type</span></span>                                                                         | <span data-ttu-id="cc1a9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc1a9-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="cc1a9-111">**modello**</span><span class="sxs-lookup"><span data-stu-id="cc1a9-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="cc1a9-112">**TemplateItemType**</span><span class="sxs-lookup"><span data-stu-id="cc1a9-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="cc1a9-113">Modello che definisce i dati da includere in un evento.</span><span class="sxs-lookup"><span data-stu-id="cc1a9-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cc1a9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc1a9-114">Requirements</span></span>



| <span data-ttu-id="cc1a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc1a9-115">Requirement</span></span> | <span data-ttu-id="cc1a9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cc1a9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc1a9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc1a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc1a9-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc1a9-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cc1a9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc1a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc1a9-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc1a9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





