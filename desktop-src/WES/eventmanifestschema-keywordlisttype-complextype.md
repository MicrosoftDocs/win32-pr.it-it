---
title: Tipo complesso KeywordListType
description: Definisce un elenco di parole chiave che categorizzano gli eventi. | Tipo complesso KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Log eventi di tipo complesso KeywordListType
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321530"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="44d9b-105">Tipo complesso KeywordListType</span><span class="sxs-lookup"><span data-stu-id="44d9b-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="44d9b-106">Definisce un elenco di parole chiave che categorizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="44d9b-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="44d9b-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="44d9b-107">Child elements</span></span>



| <span data-ttu-id="44d9b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="44d9b-108">Element</span></span>                                                                | <span data-ttu-id="44d9b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="44d9b-109">Type</span></span>                                                               | <span data-ttu-id="44d9b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44d9b-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44d9b-111">**parola chiave**</span><span class="sxs-lookup"><span data-stu-id="44d9b-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="44d9b-112">**KeywordType**</span><span class="sxs-lookup"><span data-stu-id="44d9b-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="44d9b-113">Definisce una parola chiave che identifica una categoria di eventi.</span><span class="sxs-lookup"><span data-stu-id="44d9b-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="44d9b-114">È possibile specificare un massimo di 48 parole chiave.</span><span class="sxs-lookup"><span data-stu-id="44d9b-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="44d9b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44d9b-115">Requirements</span></span>



| <span data-ttu-id="44d9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44d9b-116">Requirement</span></span> | <span data-ttu-id="44d9b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="44d9b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44d9b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44d9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44d9b-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44d9b-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44d9b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44d9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44d9b-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44d9b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





