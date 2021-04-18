---
title: Mediacollection. getPlaylistByQuery, metodo
description: Il metodo getPlaylistByQuery recupera un oggetto playlist contenente oggetti multimediali che corrispondono alle condizioni della query.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Metodo getPlaylistByQuery Windows Media Player
- Metodo getPlaylistByQuery Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327166"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="8efbd-106">Mediacollection. getPlaylistByQuery, metodo</span><span class="sxs-lookup"><span data-stu-id="8efbd-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="8efbd-107">Il metodo **getPlaylistByQuery** recupera un oggetto **playlist** contenente oggetti **multimediali** che corrispondono alle condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="8efbd-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efbd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8efbd-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="8efbd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8efbd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efbd-110">*query* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8efbd-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efbd-111">Oggetto **query** che definisce le condizioni utilizzate per creare la playlist.</span><span class="sxs-lookup"><span data-stu-id="8efbd-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="8efbd-112">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efbd-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efbd-113">**Stringa** che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8efbd-113">**String** containing the media type.</span></span> <span data-ttu-id="8efbd-114">Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="8efbd-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="8efbd-115">*sortAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efbd-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efbd-116">**Stringa** contenente il nome dell'attributo utilizzato per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8efbd-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="8efbd-117">Una stringa vuota ("") indica che non viene applicato alcun ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8efbd-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="8efbd-118">*SortAscending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efbd-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efbd-119">**Booleano**, true che indica che la playlist deve essere ordinata in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="8efbd-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efbd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8efbd-120">Return value</span></span>

<span data-ttu-id="8efbd-121">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="8efbd-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8efbd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8efbd-122">Remarks</span></span>

<span data-ttu-id="8efbd-123">Le query composte con **query** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="8efbd-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="8efbd-124">Quando la query composta specificata dal parametro di *query* contiene una condizione basata sull'attributo **mediaType** , tale condizione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8efbd-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="8efbd-125">Viene sempre usato il valore per il parametro *mediaType* .</span><span class="sxs-lookup"><span data-stu-id="8efbd-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="8efbd-126">Se, ad esempio, la query composta contiene la condizione "MediaType Equals audio" e il valore per il parametro *mediaType* è "video", la playlist risultante conterrà solo elementi video.</span><span class="sxs-lookup"><span data-stu-id="8efbd-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efbd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8efbd-127">Requirements</span></span>



| <span data-ttu-id="8efbd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8efbd-128">Requirement</span></span> | <span data-ttu-id="8efbd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8efbd-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8efbd-130">Versione</span><span class="sxs-lookup"><span data-stu-id="8efbd-130">Version</span></span><br/> | <span data-ttu-id="8efbd-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8efbd-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8efbd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8efbd-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="8efbd-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8efbd-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8efbd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8efbd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efbd-135">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="8efbd-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="8efbd-136">**Attributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="8efbd-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="8efbd-137">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="8efbd-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





