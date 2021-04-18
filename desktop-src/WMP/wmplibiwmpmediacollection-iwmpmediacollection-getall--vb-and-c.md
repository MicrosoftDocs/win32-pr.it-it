---
title: Metodo IWMPMediaCollection getAll
description: Il metodo getAll restituisce un'interfaccia IWMPPlaylist che corrisponde alla playlist che contiene tutti gli elementi multimediali nella libreria.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- Metodo getAll Windows Media Player
- Metodo getAll Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getAll
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324363"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="5e486-106">Metodo IWMPMediaCollection:: getAll</span><span class="sxs-lookup"><span data-stu-id="5e486-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="5e486-107">Il metodo **GetAll** restituisce un'interfaccia **IWMPPlaylist** che corrisponde alla playlist che contiene tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="5e486-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e486-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e486-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="5e486-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e486-109">Parameters</span></span>

<span data-ttu-id="5e486-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5e486-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e486-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e486-111">Return value</span></span>

<span data-ttu-id="5e486-112">Interfaccia **wmplib. IWMPPlaylist** per la playlist che contiene tutti gli elementi multimediali richiesti.</span><span class="sxs-lookup"><span data-stu-id="5e486-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e486-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e486-113">Remarks</span></span>

<span data-ttu-id="5e486-114">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="5e486-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="5e486-115">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5e486-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5e486-116">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del metodo **GetAll** dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="5e486-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="5e486-117">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il metodo **GetAll** restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="5e486-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="5e486-118">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo **GetAll** restituisce solo gli elementi audio nella libreria.</span><span class="sxs-lookup"><span data-stu-id="5e486-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="5e486-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5e486-119">Examples</span></span>

<span data-ttu-id="5e486-120">Nell'esempio seguente viene usato **GetAll** per riprodurre gli elementi multimediali in modo casuale dalla raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="5e486-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="5e486-121">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="5e486-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="5e486-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e486-122">Requirements</span></span>



| <span data-ttu-id="5e486-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e486-123">Requirement</span></span> | <span data-ttu-id="5e486-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5e486-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e486-125">Versione</span><span class="sxs-lookup"><span data-stu-id="5e486-125">Version</span></span><br/>   | <span data-ttu-id="5e486-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5e486-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5e486-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e486-127">Namespace</span></span><br/> | <span data-ttu-id="5e486-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5e486-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5e486-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="5e486-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5e486-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5e486-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e486-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e486-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e486-132">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5e486-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5e486-133">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5e486-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





