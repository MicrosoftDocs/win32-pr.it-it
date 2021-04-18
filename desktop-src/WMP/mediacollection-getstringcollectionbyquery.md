---
title: Mediacollection. getStringCollectionByQuery, metodo
description: Il metodo getStringCollectionByQuery recupera un oggetto StringCollection che contiene tutte le stringhe che soddisfano le condizioni della query.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Metodo getStringCollectionByQuery Windows Media Player
- Metodo getStringCollectionByQuery Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327165"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="90226-106">Mediacollection. getStringCollectionByQuery, metodo</span><span class="sxs-lookup"><span data-stu-id="90226-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="90226-107">Il metodo **getStringCollectionByQuery** recupera un oggetto **StringCollection** che contiene tutte le stringhe che soddisfano le condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="90226-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="90226-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90226-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="90226-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="90226-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90226-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90226-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90226-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="90226-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="90226-112">*query* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="90226-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90226-113">Oggetto **query** .</span><span class="sxs-lookup"><span data-stu-id="90226-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="90226-114">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90226-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90226-115">**Stringa** che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="90226-115">**String** containing the media type.</span></span> <span data-ttu-id="90226-116">Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="90226-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="90226-117">*sortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90226-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90226-118">**Stringa** contenente il nome dell'attributo utilizzato per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="90226-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="90226-119">Una stringa vuota ("") indica che non viene applicato alcun ordinamento.</span><span class="sxs-lookup"><span data-stu-id="90226-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="90226-120">*SortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90226-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90226-121">**Booleano**, true che indica che l'oggetto **StringCollection** deve essere ordinato in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="90226-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90226-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90226-122">Return value</span></span>

<span data-ttu-id="90226-123">Questo metodo restituisce un oggetto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="90226-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="90226-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="90226-124">Remarks</span></span>

<span data-ttu-id="90226-125">Le query composte con **query** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="90226-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="90226-126">Quando la query composta specificata dal parametro di *query* contiene una condizione basata sull'attributo **mediaType** , tale condizione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="90226-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="90226-127">Viene sempre usato il valore per il parametro *mediaType* .</span><span class="sxs-lookup"><span data-stu-id="90226-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="90226-128">Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *mediaType* è "video", la playlist risultante conterrà solo elementi video.</span><span class="sxs-lookup"><span data-stu-id="90226-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="90226-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90226-129">Requirements</span></span>



| <span data-ttu-id="90226-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="90226-130">Requirement</span></span> | <span data-ttu-id="90226-131">Valore</span><span class="sxs-lookup"><span data-stu-id="90226-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90226-132">Versione</span><span class="sxs-lookup"><span data-stu-id="90226-132">Version</span></span><br/> | <span data-ttu-id="90226-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="90226-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="90226-134">DLL</span><span class="sxs-lookup"><span data-stu-id="90226-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="90226-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90226-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90226-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90226-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90226-137">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="90226-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="90226-138">**Attributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="90226-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="90226-139">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="90226-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





