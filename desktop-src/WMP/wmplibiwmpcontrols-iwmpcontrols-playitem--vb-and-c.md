---
title: Metodo IWMPControls playItem
description: Il metodo playItem riproduce l'elemento multimediale specificato. | Metodo IWMPControls playItem
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- Metodo playItem Windows Media Player
- Metodo playItem Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo playItem
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332471"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="67ce2-107">IWMPControls::p metodo layItem</span><span class="sxs-lookup"><span data-stu-id="67ce2-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="67ce2-108">Il metodo **playItem** riproduce l'elemento multimediale specificato.</span><span class="sxs-lookup"><span data-stu-id="67ce2-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ce2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67ce2-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="67ce2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="67ce2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ce2-111">*pIWMPMedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67ce2-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67ce2-112">Interfaccia **wmplib. IWMPMedia** per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="67ce2-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ce2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67ce2-113">Return value</span></span>

<span data-ttu-id="67ce2-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="67ce2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ce2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="67ce2-115">Remarks</span></span>

<span data-ttu-id="67ce2-116">L'elemento multimediale verrà caricato e riprodotto automaticamente, indipendentemente dal valore della proprietà **IWMPSettings. autostart** .</span><span class="sxs-lookup"><span data-stu-id="67ce2-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="67ce2-117">Per caricare un elemento senza riprodurlo automaticamente, impostare **IWMPSettings. autostart** su **false** e assegnare un valore a **AxWindowsMediaPlayer. URL**, dopo il quale è possibile chiamare **IWMPControls. Play** per avviare la riproduzione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="67ce2-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="67ce2-118">Nota</span><span class="sxs-lookup"><span data-stu-id="67ce2-118">Note</span></span>

<span data-ttu-id="67ce2-119">**playItem** funziona solo con gli elementi in **AxWindowsMediaPlayer. currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="67ce2-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="67ce2-120">La chiamata di **playItem** con un riferimento a un elemento multimediale salvato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="67ce2-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="67ce2-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="67ce2-121">Examples</span></span>

<span data-ttu-id="67ce2-122">Nell'esempio seguente viene usato **playItem** per riprodurre un elemento multimediale dalla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="67ce2-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="67ce2-123">L'elemento da riprodurre viene scelto in base alla relativa posizione nella playlist.</span><span class="sxs-lookup"><span data-stu-id="67ce2-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="67ce2-124">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="67ce2-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="67ce2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67ce2-125">Requirements</span></span>



| <span data-ttu-id="67ce2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ce2-126">Requirement</span></span> | <span data-ttu-id="67ce2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="67ce2-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ce2-128">Versione</span><span class="sxs-lookup"><span data-stu-id="67ce2-128">Version</span></span><br/>   | <span data-ttu-id="67ce2-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="67ce2-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="67ce2-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67ce2-130">Namespace</span></span><br/> | <span data-ttu-id="67ce2-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="67ce2-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="67ce2-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="67ce2-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="67ce2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="67ce2-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ce2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67ce2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ce2-135">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67ce2-136">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67ce2-137">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67ce2-138">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67ce2-139">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67ce2-140">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67ce2-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





