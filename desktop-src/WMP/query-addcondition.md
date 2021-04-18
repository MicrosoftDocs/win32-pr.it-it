---
title: Metodo query. addCondition
description: Il metodo addCondition aggiunge una condizione all'oggetto query usando la logica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Metodo addCondition Windows Media Player
- Metodo addCondition Media Player Windows, classe query
- Classe di query Windows Media Player, metodo addCondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325984"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="76a46-106">Metodo query. addCondition</span><span class="sxs-lookup"><span data-stu-id="76a46-106">Query.addCondition method</span></span>

<span data-ttu-id="76a46-107">Il metodo **addCondition** aggiunge una condizione all'oggetto **query** usando la logica and.</span><span class="sxs-lookup"><span data-stu-id="76a46-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76a46-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="76a46-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76a46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a46-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76a46-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a46-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="76a46-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="76a46-112">*operatore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="76a46-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a46-113">**Stringa** contenente l'operatore.</span><span class="sxs-lookup"><span data-stu-id="76a46-113">**String** containing the operator.</span></span> <span data-ttu-id="76a46-114">Vedere la sezione Osservazioni per i valori supportati.</span><span class="sxs-lookup"><span data-stu-id="76a46-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="76a46-115">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="76a46-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76a46-116">**Stringa** contenente il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="76a46-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a46-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76a46-117">Return value</span></span>

<span data-ttu-id="76a46-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="76a46-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76a46-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="76a46-119">Remarks</span></span>

<span data-ttu-id="76a46-120">Le query composte con **query** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="76a46-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="76a46-121">Un elenco di valori per il parametro *attribute* è reperibile nella sezione [riferimento all'attributo alfabetico](alphabetical-attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="76a46-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="76a46-122">Le condizioni contenute in un oggetto **query** sono organizzate in gruppi di condizioni.</span><span class="sxs-lookup"><span data-stu-id="76a46-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="76a46-123">Più condizioni all'interno di un gruppo di condizioni sono sempre concatenate usando e la logica.</span><span class="sxs-lookup"><span data-stu-id="76a46-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="76a46-124">I gruppi di condizioni sono sempre concatenati l'uno all'altro usando la logica o.</span><span class="sxs-lookup"><span data-stu-id="76a46-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="76a46-125">Per avviare un nuovo gruppo di condizioni, chiamare **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="76a46-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="76a46-126">Nella tabella seguente sono elencati i valori supportati per *operator*.</span><span class="sxs-lookup"><span data-stu-id="76a46-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="76a46-127">Operatore</span><span class="sxs-lookup"><span data-stu-id="76a46-127">Operator</span></span>            | <span data-ttu-id="76a46-128">Si applica a</span><span class="sxs-lookup"><span data-stu-id="76a46-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="76a46-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="76a46-129">BeginsWith</span></span>          | <span data-ttu-id="76a46-130">Stringhe</span><span class="sxs-lookup"><span data-stu-id="76a46-130">Strings</span></span>        |
| <span data-ttu-id="76a46-131">Contiene</span><span class="sxs-lookup"><span data-stu-id="76a46-131">Contains</span></span>            | <span data-ttu-id="76a46-132">Stringhe</span><span class="sxs-lookup"><span data-stu-id="76a46-132">Strings</span></span>        |
| <span data-ttu-id="76a46-133">Uguale a</span><span class="sxs-lookup"><span data-stu-id="76a46-133">Equals</span></span>              | <span data-ttu-id="76a46-134">Tutti i tipi</span><span class="sxs-lookup"><span data-stu-id="76a46-134">All types</span></span>      |
| <span data-ttu-id="76a46-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="76a46-135">GreaterThan</span></span>         | <span data-ttu-id="76a46-136">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="76a46-136">Numbers, Dates</span></span> |
| <span data-ttu-id="76a46-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="76a46-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="76a46-138">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="76a46-138">Numbers, Dates</span></span> |
| <span data-ttu-id="76a46-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="76a46-139">LessThan</span></span>            | <span data-ttu-id="76a46-140">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="76a46-140">Numbers, Dates</span></span> |
| <span data-ttu-id="76a46-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="76a46-141">LessThanOrEquals</span></span>    | <span data-ttu-id="76a46-142">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="76a46-142">Numbers, Dates</span></span> |
| <span data-ttu-id="76a46-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="76a46-143">NotBeginsWith</span></span>       | <span data-ttu-id="76a46-144">Stringhe</span><span class="sxs-lookup"><span data-stu-id="76a46-144">Strings</span></span>        |
| <span data-ttu-id="76a46-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="76a46-145">NotContains</span></span>         | <span data-ttu-id="76a46-146">Stringhe</span><span class="sxs-lookup"><span data-stu-id="76a46-146">Strings</span></span>        |
| <span data-ttu-id="76a46-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="76a46-147">NotEquals</span></span>           | <span data-ttu-id="76a46-148">Tutti i tipi</span><span class="sxs-lookup"><span data-stu-id="76a46-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="76a46-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="76a46-149">Examples</span></span>

<span data-ttu-id="76a46-150">Nell'esempio JScript seguente vengono utilizzati **query. addCondition** e **query. beginNextGroup** per eseguire una query di esempio.</span><span class="sxs-lookup"><span data-stu-id="76a46-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="76a46-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76a46-151">Requirements</span></span>



| <span data-ttu-id="76a46-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="76a46-152">Requirement</span></span> | <span data-ttu-id="76a46-153">Valore</span><span class="sxs-lookup"><span data-stu-id="76a46-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76a46-154">Versione</span><span class="sxs-lookup"><span data-stu-id="76a46-154">Version</span></span><br/> | <span data-ttu-id="76a46-155">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="76a46-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="76a46-156">DLL</span><span class="sxs-lookup"><span data-stu-id="76a46-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="76a46-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76a46-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76a46-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76a46-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a46-159">**Mediacollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="76a46-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="76a46-160">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="76a46-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="76a46-161">**Mediacollection. getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="76a46-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="76a46-162">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="76a46-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="76a46-163">**Query. beginNextGroup**</span><span class="sxs-lookup"><span data-stu-id="76a46-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





