---
title: Metodo IWMPQuery addCondition
description: Il metodo addCondition aggiunge una condizione alla query composta usando la logica AND.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- Metodo addCondition Windows Media Player
- Metodo addCondition Windows Media Player, interfaccia IWMPQuery
- Interfaccia IWMPQuery Windows Media Player, metodo addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330451"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="ad1d8-106">Metodo IWMPQuery:: addCondition</span><span class="sxs-lookup"><span data-stu-id="ad1d8-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="ad1d8-107">Il metodo **addCondition** aggiunge una condizione alla query composta usando la logica **and** .</span><span class="sxs-lookup"><span data-stu-id="ad1d8-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad1d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad1d8-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="ad1d8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad1d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad1d8-110">*bstrAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad1d8-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad1d8-111">**System. String** che rappresenta il nome dell'attributo da aggiungere alla query.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="ad1d8-112">*bstrOperator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad1d8-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad1d8-113">**System. String** che rappresenta l'operatore.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="ad1d8-114">Vedere la sezione Osservazioni per i valori supportati.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="ad1d8-115">*bstrValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad1d8-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad1d8-116">**System. String** che corrisponde al valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad1d8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad1d8-117">Return value</span></span>

<span data-ttu-id="ad1d8-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad1d8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad1d8-119">Remarks</span></span>

<span data-ttu-id="ad1d8-120">Le condizioni contenute in una query composta sono organizzate in gruppi di condizioni.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="ad1d8-121">Più condizioni all'interno di un gruppo di condizioni sono sempre concatenate usando **e** la logica.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="ad1d8-122">I gruppi di condizioni sono sempre concatenati tra loro tramite **o** la logica.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="ad1d8-123">Per avviare un nuovo gruppo di condizioni, chiamare [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="ad1d8-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="ad1d8-124">Le query composte con **IWMPQuery** non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="ad1d8-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="ad1d8-125">È possibile trovare un elenco di valori per il parametro *bstrAttribute* in [riferimento all'attributo alfabetico](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ad1d8-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="ad1d8-126">Nella tabella seguente sono elencati i valori supportati per *bstrOperator*.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="ad1d8-127">string</span><span class="sxs-lookup"><span data-stu-id="ad1d8-127">String</span></span>              | <span data-ttu-id="ad1d8-128">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ad1d8-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="ad1d8-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="ad1d8-129">BeginsWith</span></span>          | <span data-ttu-id="ad1d8-130">Stringhe</span><span class="sxs-lookup"><span data-stu-id="ad1d8-130">Strings</span></span>        |
| <span data-ttu-id="ad1d8-131">Contiene</span><span class="sxs-lookup"><span data-stu-id="ad1d8-131">Contains</span></span>            | <span data-ttu-id="ad1d8-132">Stringhe</span><span class="sxs-lookup"><span data-stu-id="ad1d8-132">Strings</span></span>        |
| <span data-ttu-id="ad1d8-133">Uguale a</span><span class="sxs-lookup"><span data-stu-id="ad1d8-133">Equals</span></span>              | <span data-ttu-id="ad1d8-134">Tutti i tipi</span><span class="sxs-lookup"><span data-stu-id="ad1d8-134">All types</span></span>      |
| <span data-ttu-id="ad1d8-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ad1d8-135">GreaterThan</span></span>         | <span data-ttu-id="ad1d8-136">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="ad1d8-136">Numbers, Dates</span></span> |
| <span data-ttu-id="ad1d8-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="ad1d8-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="ad1d8-138">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="ad1d8-138">Numbers, Dates</span></span> |
| <span data-ttu-id="ad1d8-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="ad1d8-139">LessThan</span></span>            | <span data-ttu-id="ad1d8-140">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="ad1d8-140">Numbers, Dates</span></span> |
| <span data-ttu-id="ad1d8-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="ad1d8-141">LessThanOrEquals</span></span>    | <span data-ttu-id="ad1d8-142">Numeri, date</span><span class="sxs-lookup"><span data-stu-id="ad1d8-142">Numbers, Dates</span></span> |
| <span data-ttu-id="ad1d8-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ad1d8-143">NotBeginsWith</span></span>       | <span data-ttu-id="ad1d8-144">Stringhe</span><span class="sxs-lookup"><span data-stu-id="ad1d8-144">Strings</span></span>        |
| <span data-ttu-id="ad1d8-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="ad1d8-145">NotContains</span></span>         | <span data-ttu-id="ad1d8-146">Stringhe</span><span class="sxs-lookup"><span data-stu-id="ad1d8-146">Strings</span></span>        |
| <span data-ttu-id="ad1d8-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="ad1d8-147">NotEquals</span></span>           | <span data-ttu-id="ad1d8-148">Tutti i tipi</span><span class="sxs-lookup"><span data-stu-id="ad1d8-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="ad1d8-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad1d8-149">Examples</span></span>

<span data-ttu-id="ad1d8-150">Nell'esempio seguente viene creata una query, vengono aggiunte due condizioni e viene utilizzata la query per estrarre i risultati della query come raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="ad1d8-151">I risultati vengono quindi visualizzati in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="ad1d8-152">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="ad1d8-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad1d8-153">Requirements</span></span>



| <span data-ttu-id="ad1d8-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad1d8-154">Requirement</span></span> | <span data-ttu-id="ad1d8-155">Valore</span><span class="sxs-lookup"><span data-stu-id="ad1d8-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1d8-156">Versione</span><span class="sxs-lookup"><span data-stu-id="ad1d8-156">Version</span></span><br/>   | <span data-ttu-id="ad1d8-157">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ad1d8-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ad1d8-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad1d8-158">Namespace</span></span><br/> | <span data-ttu-id="ad1d8-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ad1d8-160">Assembly</span><span class="sxs-lookup"><span data-stu-id="ad1d8-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ad1d8-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ad1d8-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad1d8-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad1d8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1d8-163">**Riferimento alfabetico agli attributi**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="ad1d8-164">**IWMPMediaCollection2. createQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ad1d8-165">**IWMPMediaCollection2. getPlaylistByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ad1d8-166">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ad1d8-167">**Interfaccia IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="ad1d8-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





