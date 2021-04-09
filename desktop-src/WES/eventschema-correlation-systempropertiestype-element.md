---
title: Elemento Correlation (SystemPropertiesType)
description: Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- EventLog elemento correlazione
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964669"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="af007-104">Elemento Correlation (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="af007-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="af007-105">Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.</span><span class="sxs-lookup"><span data-stu-id="af007-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="af007-106">L'elemento **correlazione** viene definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="af007-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="af007-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="af007-107">Attributes</span></span>



| <span data-ttu-id="af007-108">Nome</span><span class="sxs-lookup"><span data-stu-id="af007-108">Name</span></span>              | <span data-ttu-id="af007-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="af007-109">Type</span></span>                                                | <span data-ttu-id="af007-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af007-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af007-111">ActivityID</span><span class="sxs-lookup"><span data-stu-id="af007-111">ActivityID</span></span>        | [<span data-ttu-id="af007-112">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="af007-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="af007-113">Identificatore univoco globale che identifica l'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="af007-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="af007-114">Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.</span><span class="sxs-lookup"><span data-stu-id="af007-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="af007-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="af007-115">RelatedActivityID</span></span> | [<span data-ttu-id="af007-116">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="af007-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="af007-117">Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo.</span><span class="sxs-lookup"><span data-stu-id="af007-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="af007-118">Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.</span><span class="sxs-lookup"><span data-stu-id="af007-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="af007-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af007-119">Requirements</span></span>



| <span data-ttu-id="af007-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="af007-120">Requirement</span></span> | <span data-ttu-id="af007-121">Valore</span><span class="sxs-lookup"><span data-stu-id="af007-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af007-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af007-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af007-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af007-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af007-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af007-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af007-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af007-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af007-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af007-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="af007-127">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="af007-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="af007-128">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="af007-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





