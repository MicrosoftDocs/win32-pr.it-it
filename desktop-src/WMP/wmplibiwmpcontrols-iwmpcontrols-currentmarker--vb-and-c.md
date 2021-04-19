---
title: Proprietà currentMarker di IWMPControls
description: La proprietà currentMarker Ottiene o imposta il numero di marcatore corrente.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Finestra delle proprietà di currentMarker Media Player
- Proprietà di currentMarker Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332489"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="4a342-106">Proprietà IWMPControls:: currentMarker</span><span class="sxs-lookup"><span data-stu-id="4a342-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="4a342-107">La proprietà **currentMarker** Ottiene o imposta il numero di marcatore corrente.</span><span class="sxs-lookup"><span data-stu-id="4a342-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a342-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a342-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="4a342-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4a342-109">Property value</span></span>

<span data-ttu-id="4a342-110">**System. Int32** che rappresenta il numero del marcatore.</span><span class="sxs-lookup"><span data-stu-id="4a342-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a342-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a342-111">Remarks</span></span>

<span data-ttu-id="4a342-112">L'impostazione di **currentMarker** fa sì che la riproduzione venga avviata dal marcatore specificato.</span><span class="sxs-lookup"><span data-stu-id="4a342-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="4a342-113">Prima di provare a impostare **currentMarker**, determinare se un file contiene marcatori e il numero di marcatori utilizzando **IWMPMedia. markerCount**.</span><span class="sxs-lookup"><span data-stu-id="4a342-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="4a342-114">Se un file non ha marcatori, l'impostazione di **currentMarker** su qualsiasi elemento, ma con zero, genera un errore.</span><span class="sxs-lookup"><span data-stu-id="4a342-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="4a342-115">L'impostazione di **currentMarker** su un numero maggiore di **markerCount** genera anche un errore.</span><span class="sxs-lookup"><span data-stu-id="4a342-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="4a342-116">La proprietà **currentMarker** restituisce sempre il marcatore corrente o ultimo, il che significa che la posizione effettiva del file può essere in corrispondenza del marcatore corrente o prima del marcatore successivo.</span><span class="sxs-lookup"><span data-stu-id="4a342-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="4a342-117">I marcatori sono numerati a partire da 1, pertanto se un file contiene marcatori, è possibile impostare **currentMarker** su zero per modificare la posizione del file su zero.</span><span class="sxs-lookup"><span data-stu-id="4a342-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="4a342-118">Fino a quando non viene impostato l'elemento multimediale corrente (usando **AxWindowsMediaPlayer. URL** o **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4a342-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="4a342-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="4a342-119">Examples</span></span>

<span data-ttu-id="4a342-120">Nell'esempio seguente viene usato **currentMarker** per avviare la riproduzione video dal marcatore che corrisponde alla proprietà SelectedIndex di una casella di riepilogo che è stata riempita con identificatori del marcatore.</span><span class="sxs-lookup"><span data-stu-id="4a342-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="4a342-121">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="4a342-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4a342-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a342-122">Requirements</span></span>



| <span data-ttu-id="4a342-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a342-123">Requirement</span></span> | <span data-ttu-id="4a342-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4a342-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a342-125">Versione</span><span class="sxs-lookup"><span data-stu-id="4a342-125">Version</span></span><br/>   | <span data-ttu-id="4a342-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4a342-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4a342-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a342-127">Namespace</span></span><br/> | <span data-ttu-id="4a342-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4a342-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4a342-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="4a342-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4a342-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4a342-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a342-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a342-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a342-132">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4a342-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4a342-133">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4a342-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4a342-134">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4a342-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4a342-135">**IWMPMedia. markerCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4a342-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





