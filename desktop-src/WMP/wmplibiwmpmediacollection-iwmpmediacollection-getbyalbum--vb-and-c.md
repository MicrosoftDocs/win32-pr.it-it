---
title: Metodo IWMPMediaCollection getByAlbum
description: Il metodo getByAlbum restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali dall'album specificato.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- Metodo getByAlbum Windows Media Player
- Metodo getByAlbum Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333644"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="c3357-106">Metodo IWMPMediaCollection:: getByAlbum</span><span class="sxs-lookup"><span data-stu-id="c3357-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="c3357-107">Il metodo **getByAlbum** restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'album specificato.</span><span class="sxs-lookup"><span data-stu-id="c3357-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3357-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3357-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="c3357-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3357-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3357-110">*bstrAlbum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3357-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3357-111">**System. String** che rappresenta il titolo dell'album.</span><span class="sxs-lookup"><span data-stu-id="c3357-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3357-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3357-112">Return value</span></span>

<span data-ttu-id="c3357-113">Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.</span><span class="sxs-lookup"><span data-stu-id="c3357-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3357-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3357-114">Remarks</span></span>

<span data-ttu-id="c3357-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c3357-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c3357-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c3357-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c3357-117">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del metodo **getByAlbum** dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="c3357-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="c3357-118">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il metodo **getByAlbum** restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="c3357-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="c3357-119">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo **getByAlbum** restituisce solo gli elementi audio della libreria che appartengono all'album specificato.</span><span class="sxs-lookup"><span data-stu-id="c3357-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="c3357-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="c3357-120">Examples</span></span>

<span data-ttu-id="c3357-121">Nell'esempio seguente viene usato **getByAlbum** per creare una playlist di elementi multimediali quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="c3357-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="c3357-122">La playlist contiene elementi con l'album specificato dall'utente in una casella di testo.</span><span class="sxs-lookup"><span data-stu-id="c3357-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="c3357-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c3357-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c3357-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3357-124">Requirements</span></span>



| <span data-ttu-id="c3357-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3357-125">Requirement</span></span> | <span data-ttu-id="c3357-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c3357-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3357-127">Versione</span><span class="sxs-lookup"><span data-stu-id="c3357-127">Version</span></span><br/>   | <span data-ttu-id="c3357-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c3357-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c3357-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3357-129">Namespace</span></span><br/> | <span data-ttu-id="c3357-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3357-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c3357-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3357-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3357-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3357-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3357-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3357-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3357-134">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3357-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3357-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3357-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





