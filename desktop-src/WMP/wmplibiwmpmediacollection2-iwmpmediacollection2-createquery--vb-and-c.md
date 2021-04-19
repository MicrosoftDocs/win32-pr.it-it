---
title: Metodo IWMPMediaCollection2 createQuery
description: Il metodo createQuery restituisce un'interfaccia IWMPQuery che rappresenta una nuova query.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- metodo createQuery Windows Media Player
- metodo createQuery Windows Media Player, interfaccia IWMPMediaCollection2
- Interfaccia IWMPMediaCollection2 Windows Media Player, metodo createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333397"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="8a441-106">Metodo IWMPMediaCollection2:: createQuery</span><span class="sxs-lookup"><span data-stu-id="8a441-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="8a441-107">Il `createQuery` metodo restituisce un'interfaccia **IWMPQuery** che rappresenta una nuova query.</span><span class="sxs-lookup"><span data-stu-id="8a441-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a441-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a441-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="8a441-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a441-109">Parameters</span></span>

<span data-ttu-id="8a441-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8a441-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a441-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a441-111">Return value</span></span>

<span data-ttu-id="8a441-112">Interfaccia **wmplib. IWMPQuery** che rappresenta una nuova query vuota.</span><span class="sxs-lookup"><span data-stu-id="8a441-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a441-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a441-113">Remarks</span></span>

<span data-ttu-id="8a441-114">La creazione di una nuova query rappresenta il primo passaggio per la creazione di una query composta.</span><span class="sxs-lookup"><span data-stu-id="8a441-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="8a441-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a441-115">Examples</span></span>

<span data-ttu-id="8a441-116">Nell'esempio seguente viene usato `createQuery` per ottenere un'interfaccia **IWMPQuery** inizializzata su null.</span><span class="sxs-lookup"><span data-stu-id="8a441-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="8a441-117">Poiché a questa query non sono state aggiunte condizioni, quando viene usato come argomento nel metodo **getStringCollectionByQuery** , il metodo restituisce una raccolta di stringhe che contiene tutti gli elementi multimediali del tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="8a441-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="8a441-118">La raccolta di stringhe viene quindi visualizzata in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="8a441-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="8a441-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a441-119">Requirements</span></span>



| <span data-ttu-id="8a441-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a441-120">Requirement</span></span> | <span data-ttu-id="8a441-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8a441-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a441-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8a441-122">Version</span></span><br/>   | <span data-ttu-id="8a441-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8a441-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="8a441-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a441-124">Namespace</span></span><br/> | <span data-ttu-id="8a441-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8a441-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8a441-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="8a441-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8a441-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8a441-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a441-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a441-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a441-129">**Interfaccia IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8a441-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8a441-130">**Interfaccia IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8a441-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





