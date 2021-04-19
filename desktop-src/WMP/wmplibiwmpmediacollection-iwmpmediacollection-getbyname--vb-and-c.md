---
title: IWMPMediaCollection (metodo getByName)
description: Il metodo getByName restituisce un'interfaccia IWMPPlaylist che consente di accedere agli elementi multimediali con il nome specificato.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- metodo getByName Media Player Windows
- metodo getByName Media Player Windows, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByName
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333405"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="e3ee4-106">Metodo IWMPMediaCollection:: getByName</span><span class="sxs-lookup"><span data-stu-id="e3ee4-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="e3ee4-107">Il `getByName` metodo restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ee4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3ee4-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="e3ee4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3ee4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ee4-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3ee4-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ee4-111">**System. String** che rappresenta il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ee4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3ee4-112">Return value</span></span>

<span data-ttu-id="e3ee4-113">Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ee4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3ee4-114">Remarks</span></span>

<span data-ttu-id="e3ee4-115">Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e3ee4-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e3ee4-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e3ee4-117">Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del `getByName` metodo dipende da quali di questi due modi si usano.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="e3ee4-118">Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il `getByName` metodo restituisce tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="e3ee4-119">Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il `getByName` metodo restituisce solo gli elementi audio della raccolta con l'attributo e il valore specificati.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="e3ee4-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="e3ee4-120">Examples</span></span>

<span data-ttu-id="e3ee4-121">Nell'esempio seguente viene usato `getByName` per recuperare tre elementi dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="e3ee4-122">Ogni elemento viene quindi aggiunto alla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="e3ee4-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="e3ee4-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="e3ee4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3ee4-124">Requirements</span></span>



| <span data-ttu-id="e3ee4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ee4-125">Requirement</span></span> | <span data-ttu-id="e3ee4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e3ee4-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ee4-127">Versione</span><span class="sxs-lookup"><span data-stu-id="e3ee4-127">Version</span></span><br/>   | <span data-ttu-id="e3ee4-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e3ee4-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e3ee4-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3ee4-129">Namespace</span></span><br/> | <span data-ttu-id="e3ee4-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e3ee4-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e3ee4-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="e3ee4-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3ee4-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3ee4-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ee4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3ee4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ee4-134">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3ee4-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e3ee4-135">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e3ee4-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





