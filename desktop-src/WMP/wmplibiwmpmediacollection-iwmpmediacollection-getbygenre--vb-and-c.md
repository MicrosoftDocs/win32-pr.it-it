---
title: Metodo IWMPMediaCollection getByGenre
description: Il metodo getByGenre restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali del genere specificato.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- Metodo getByGenre Windows Media Player
- Metodo getByGenre Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332889"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="200ba-106">Metodo IWMPMediaCollection:: getByGenre</span><span class="sxs-lookup"><span data-stu-id="200ba-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="200ba-107">Il `getByGenre` metodo restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali del genere specificato.</span><span class="sxs-lookup"><span data-stu-id="200ba-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="200ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="200ba-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="200ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="200ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200ba-110">*bstrGenre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="200ba-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200ba-111">**System. String** che rappresenta il nome del genere.</span><span class="sxs-lookup"><span data-stu-id="200ba-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200ba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="200ba-112">Return value</span></span>

<span data-ttu-id="200ba-113">Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.</span><span class="sxs-lookup"><span data-stu-id="200ba-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="200ba-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="200ba-114">Remarks</span></span>

<span data-ttu-id="200ba-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="200ba-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="200ba-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="200ba-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="200ba-117">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del `getByGenre` metodo dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="200ba-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="200ba-118">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il `getByGenre` metodo restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="200ba-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="200ba-119">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il `getByGenre` metodo restituisce solo gli elementi audio della raccolta con l'attributo e il valore specificati.</span><span class="sxs-lookup"><span data-stu-id="200ba-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="200ba-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="200ba-120">Examples</span></span>

<span data-ttu-id="200ba-121">Nell'esempio seguente viene usato `getByGenre` per recuperare una playlist di elementi multimediali quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="200ba-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="200ba-122">La playlist contiene gli elementi con il genere specificato dall'utente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="200ba-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="200ba-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="200ba-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="200ba-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="200ba-124">Requirements</span></span>



| <span data-ttu-id="200ba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="200ba-125">Requirement</span></span> | <span data-ttu-id="200ba-126">Valore</span><span class="sxs-lookup"><span data-stu-id="200ba-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200ba-127">Versione</span><span class="sxs-lookup"><span data-stu-id="200ba-127">Version</span></span><br/>   | <span data-ttu-id="200ba-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="200ba-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="200ba-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="200ba-129">Namespace</span></span><br/> | <span data-ttu-id="200ba-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="200ba-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="200ba-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="200ba-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="200ba-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="200ba-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200ba-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="200ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200ba-134">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="200ba-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="200ba-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="200ba-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





