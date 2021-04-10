---
title: Elemento di eliminazione (QueryType)
description: Query XPath che identifica gli eventi da escludere dal set di risultati della query.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Non visualizzare l'elemento EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121538"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="c9293-104">Elemento di eliminazione (QueryType)</span><span class="sxs-lookup"><span data-stu-id="c9293-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="c9293-105">Query XPath che identifica gli eventi da escludere dal set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="c9293-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="c9293-106">L'elemento di **eliminazione** viene definito dal tipo complesso [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c9293-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="c9293-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="c9293-107">Attributes</span></span>



| <span data-ttu-id="c9293-108">Nome</span><span class="sxs-lookup"><span data-stu-id="c9293-108">Name</span></span> | <span data-ttu-id="c9293-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9293-109">Type</span></span>   | <span data-ttu-id="c9293-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9293-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9293-111">Percorso</span><span class="sxs-lookup"><span data-stu-id="c9293-111">Path</span></span> | <span data-ttu-id="c9293-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="c9293-112">anyURI</span></span> | <span data-ttu-id="c9293-113">Nome del canale o percorso del file di log che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="c9293-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c9293-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9293-114">Requirements</span></span>



| <span data-ttu-id="c9293-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9293-115">Requirement</span></span> | <span data-ttu-id="c9293-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c9293-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9293-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9293-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9293-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9293-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9293-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9293-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9293-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9293-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9293-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9293-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9293-122">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="c9293-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="c9293-123">**Query (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="c9293-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





