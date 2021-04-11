---
title: Tipo complesso QueryType
description: Definisce un set di query di selezione e di eliminazione utilizzate per includere eventi in o escludere eventi dal set di risultati.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Log eventi di tipo complesso QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119682"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="f7959-104">Tipo complesso QueryType</span><span class="sxs-lookup"><span data-stu-id="f7959-104">QueryType Complex Type</span></span>

<span data-ttu-id="f7959-105">Definisce un set di query di selezione e di eliminazione utilizzate per includere eventi in o escludere eventi dal set di risultati.</span><span class="sxs-lookup"><span data-stu-id="f7959-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f7959-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f7959-106">Child elements</span></span>



| <span data-ttu-id="f7959-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7959-107">Element</span></span>                                                    | <span data-ttu-id="f7959-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7959-108">Type</span></span> | <span data-ttu-id="f7959-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7959-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7959-110">**Selezionare**</span><span class="sxs-lookup"><span data-stu-id="f7959-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="f7959-111">Query XPath che identifica gli eventi da includere nel set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="f7959-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="f7959-112">Specificare XPath nel corpo del testo di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f7959-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="f7959-113">XPath è limitato a 32 espressioni.</span><span class="sxs-lookup"><span data-stu-id="f7959-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="f7959-114">**Elimina**</span><span class="sxs-lookup"><span data-stu-id="f7959-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="f7959-115">Query XPath che identifica gli eventi da escludere dal set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="f7959-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="f7959-116">Specificare XPath nel corpo del testo di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="f7959-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="f7959-117">XPath è limitato a 32 espressioni.</span><span class="sxs-lookup"><span data-stu-id="f7959-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f7959-118">Attributi</span><span class="sxs-lookup"><span data-stu-id="f7959-118">Attributes</span></span>



| <span data-ttu-id="f7959-119">Nome</span><span class="sxs-lookup"><span data-stu-id="f7959-119">Name</span></span> | <span data-ttu-id="f7959-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7959-120">Type</span></span>   | <span data-ttu-id="f7959-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7959-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7959-122">Id</span><span class="sxs-lookup"><span data-stu-id="f7959-122">Id</span></span>   | <span data-ttu-id="f7959-123">long</span><span class="sxs-lookup"><span data-stu-id="f7959-123">long</span></span>   | <span data-ttu-id="f7959-124">Identificatore che identifica in modo univoco la query nell'elenco di query.</span><span class="sxs-lookup"><span data-stu-id="f7959-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="f7959-125">L'identificatore è in base zero.</span><span class="sxs-lookup"><span data-stu-id="f7959-125">The identifier is zero-based.</span></span> <span data-ttu-id="f7959-126">È necessario specificare un identificatore se l'elenco di query contiene più di una query.</span><span class="sxs-lookup"><span data-stu-id="f7959-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="f7959-127">Percorso</span><span class="sxs-lookup"><span data-stu-id="f7959-127">Path</span></span> | <span data-ttu-id="f7959-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="f7959-128">anyURI</span></span> | <span data-ttu-id="f7959-129">Nome del canale o percorso del file di log che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f7959-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="f7959-130">Percorso</span><span class="sxs-lookup"><span data-stu-id="f7959-130">Path</span></span> | <span data-ttu-id="f7959-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="f7959-131">anyURI</span></span> | <span data-ttu-id="f7959-132">Nome del canale o percorso del file di log che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f7959-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="f7959-133">Percorso</span><span class="sxs-lookup"><span data-stu-id="f7959-133">Path</span></span> | <span data-ttu-id="f7959-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="f7959-134">anyURI</span></span> | <span data-ttu-id="f7959-135">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f7959-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="f7959-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7959-136">Remarks</span></span>

<span data-ttu-id="f7959-137">La query deve contenere almeno un'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="f7959-137">The query must have at least one select statement.</span></span> <span data-ttu-id="f7959-138">Per ogni istruzione di eliminazione, è necessario che sia presente almeno un'istruzione SELECT che specifica lo stesso percorso.</span><span class="sxs-lookup"><span data-stu-id="f7959-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="f7959-139">Se la query di selezione e di eliminazione restituisce gli stessi eventi, l'istruzione di eliminazione avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="f7959-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="f7959-140">Se si selezionano eventi da più origini, gli eventi vengono restituiti nell'ordine del timestamp.</span><span class="sxs-lookup"><span data-stu-id="f7959-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="f7959-141">Se si usa l'indicatore di ora di sistema e la frequenza degli eventi è elevata, è possibile che più di un evento disponga dello stesso timestamp.</span><span class="sxs-lookup"><span data-stu-id="f7959-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="f7959-142">Quando si verifica questa situazione, l'ordine degli eventi diventa ambiguo e gli eventi potrebbero non essere visualizzati in ordine.</span><span class="sxs-lookup"><span data-stu-id="f7959-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="f7959-143">Se si specifica un percorso per una delle query nell'elenco di query, tutte le query devono specificare un percorso.</span><span class="sxs-lookup"><span data-stu-id="f7959-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="f7959-144">Se non si specifica un percorso per tutte le query, è necessario specificare il percorso quando si chiama la funzione [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="f7959-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7959-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7959-145">Requirements</span></span>



| <span data-ttu-id="f7959-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7959-146">Requirement</span></span> | <span data-ttu-id="f7959-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f7959-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7959-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7959-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f7959-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7959-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7959-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7959-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f7959-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7959-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





