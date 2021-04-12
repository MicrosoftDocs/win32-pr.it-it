---
title: Select (QueryType)-elemento
description: Query XPath che identifica gli eventi da includere nel set di risultati della query.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Seleziona EventLog elemento
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400868"
---
# <a name="select-querytype-element"></a><span data-ttu-id="f2842-104">Select (QueryType)-elemento</span><span class="sxs-lookup"><span data-stu-id="f2842-104">Select (QueryType) Element</span></span>

<span data-ttu-id="f2842-105">Query XPath che identifica gli eventi da includere nel set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="f2842-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f2842-106">L'elemento **Select** è definito dal tipo complesso [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2842-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="f2842-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="f2842-107">Attributes</span></span>



| <span data-ttu-id="f2842-108">Nome</span><span class="sxs-lookup"><span data-stu-id="f2842-108">Name</span></span> | <span data-ttu-id="f2842-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2842-109">Type</span></span>   | <span data-ttu-id="f2842-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2842-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2842-111">Percorso</span><span class="sxs-lookup"><span data-stu-id="f2842-111">Path</span></span> | <span data-ttu-id="f2842-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="f2842-112">anyURI</span></span> | <span data-ttu-id="f2842-113">Nome del canale o percorso del file di log che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f2842-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f2842-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2842-114">Requirements</span></span>



| <span data-ttu-id="f2842-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2842-115">Requirement</span></span> | <span data-ttu-id="f2842-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f2842-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f2842-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2842-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2842-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f2842-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="f2842-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2842-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2842-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f2842-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2842-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2842-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2842-122">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="f2842-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="f2842-123">**Query (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="f2842-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





