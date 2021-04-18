---
title: Metodo IWMPQuery beginNextGroup
description: Il metodo beginNextGroup avvia un nuovo gruppo di condizioni. | Metodo IWMPQuery beginNextGroup
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- Metodo beginNextGroup Windows Media Player
- Metodo beginNextGroup Windows Media Player, interfaccia IWMPQuery
- Interfaccia IWMPQuery Windows Media Player, metodo beginNextGroup
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330450"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="f9079-107">Metodo IWMPQuery:: beginNextGroup</span><span class="sxs-lookup"><span data-stu-id="f9079-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="f9079-108">Il metodo **beginNextGroup** avvia un nuovo gruppo di condizioni.</span><span class="sxs-lookup"><span data-stu-id="f9079-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9079-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9079-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="f9079-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9079-110">Parameters</span></span>

<span data-ttu-id="f9079-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9079-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9079-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9079-112">Return value</span></span>

<span data-ttu-id="f9079-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f9079-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9079-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9079-114">Remarks</span></span>

<span data-ttu-id="f9079-115">L'inizio di un nuovo gruppo di condizioni implica il completamento del gruppo di condizioni corrente.</span><span class="sxs-lookup"><span data-stu-id="f9079-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="f9079-116">Il nuovo gruppo di condizioni viene sempre concatenato al gruppo di condizioni precedente mediante la logica **o** .</span><span class="sxs-lookup"><span data-stu-id="f9079-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="f9079-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9079-117">Examples</span></span>

<span data-ttu-id="f9079-118">Nell'esempio seguente viene creata una query complessa mediante il combing di due gruppi che contengono una condizione.</span><span class="sxs-lookup"><span data-stu-id="f9079-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="f9079-119">I risultati della query vengono estratti come una raccolta di stringhe e visualizzati in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="f9079-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="f9079-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f9079-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="f9079-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9079-121">Requirements</span></span>



| <span data-ttu-id="f9079-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9079-122">Requirement</span></span> | <span data-ttu-id="f9079-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f9079-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9079-124">Versione</span><span class="sxs-lookup"><span data-stu-id="f9079-124">Version</span></span><br/>   | <span data-ttu-id="f9079-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f9079-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f9079-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9079-126">Namespace</span></span><br/> | <span data-ttu-id="f9079-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f9079-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f9079-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="f9079-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f9079-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f9079-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9079-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9079-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9079-131">**IWMPMediaCollection2. createQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9079-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9079-132">**IWMPMediaCollection2. getPlaylistByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9079-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9079-133">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9079-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9079-134">**Interfaccia IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9079-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





