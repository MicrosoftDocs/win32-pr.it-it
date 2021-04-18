---
title: Metodo IWMPMediaCollection getByAuthor
description: Il metodo getByAuthor restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali dall'autore specificato.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- Metodo getByAuthor Windows Media Player
- Metodo getByAuthor Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333641"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="a97a1-106">Metodo IWMPMediaCollection:: getByAuthor</span><span class="sxs-lookup"><span data-stu-id="a97a1-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="a97a1-107">Il `getByAuthor` metodo restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'autore specificato.</span><span class="sxs-lookup"><span data-stu-id="a97a1-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a97a1-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="a97a1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a97a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a97a1-110">*bstrAuthor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a97a1-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a97a1-111">**System. String** che rappresenta il nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="a97a1-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a97a1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a97a1-112">Return value</span></span>

<span data-ttu-id="a97a1-113">Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.</span><span class="sxs-lookup"><span data-stu-id="a97a1-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="a97a1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a97a1-114">Remarks</span></span>

<span data-ttu-id="a97a1-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a97a1-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a97a1-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a97a1-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a97a1-117">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del `getByAuthor` metodo dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="a97a1-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="a97a1-118">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il `getByAuthor` metodo restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="a97a1-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="a97a1-119">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il `getByAuthor` metodo restituisce solo gli elementi audio della raccolta con l'attributo e il valore specificati.</span><span class="sxs-lookup"><span data-stu-id="a97a1-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="a97a1-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="a97a1-120">Examples</span></span>

<span data-ttu-id="a97a1-121">Nell'esempio seguente viene usato `getByAuthor` per creare una playlist di elementi multimediali quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="a97a1-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="a97a1-122">La playlist contiene elementi che corrispondono al nome dell'autore specificato dall'utente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="a97a1-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="a97a1-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a97a1-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a97a1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a97a1-124">Requirements</span></span>



| <span data-ttu-id="a97a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97a1-125">Requirement</span></span> | <span data-ttu-id="a97a1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a97a1-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a97a1-127">Versione</span><span class="sxs-lookup"><span data-stu-id="a97a1-127">Version</span></span><br/>   | <span data-ttu-id="a97a1-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a97a1-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a97a1-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a97a1-129">Namespace</span></span><br/> | <span data-ttu-id="a97a1-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a97a1-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a97a1-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="a97a1-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a97a1-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a97a1-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97a1-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a97a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97a1-134">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a97a1-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a97a1-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a97a1-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





